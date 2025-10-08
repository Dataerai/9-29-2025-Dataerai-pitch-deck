<script setup lang="js">
import { computed, useSlots } from 'vue'
import { compute_alignment, compute_column_size } from '../layoutHelper'

const slots = useSlots()

const props = defineProps({
  columns: {
    default: 'is-one-third',
  },
  align: {
    default: 'l-lt-ct-rt',
  },
  color: {
    default: 'white',
  },
  titlepos: {
    default: 't',
    validator: (value) => ['t', 'b', 'n'].includes(value),
  },
})

const alignment = computed(() => {
  const parts = props.align.split('-')
  return {
    t: compute_alignment(parts[0]),
    l: compute_alignment(parts[1]),
    c: compute_alignment(parts[2]),
    r: compute_alignment(parts[3]),
  }
})

const colwidth = computed(() => compute_column_size(props.columns))

const colorscheme = computed(() => `neversink-${props.color}-scheme`)

const flexclass = computed(() => {
  if (slots.title) {
    if (props.titlepos === 't') return 'slidev-layout three-cols-header'
    if (props.titlepos === 'b') return 'slidev-layout three-cols-footer'
  }
  return 'slidev-layout three-cols'
})
</script>

<template>
  <div
    v-if="colwidth == 'error' || alignment.t == 'error' || alignment.l == 'error' || alignment.c == 'error' || alignment.r == 'error'"
    class="slidev-layout default error"
  >
    <span class="ns-c-warning"><b>Error</b>: invalid layout params.</span>
    <hr />
    <p>
      Parameters: <code>columns</code>, <code>align</code>, <code>color</code>, and <code>titlepos</code>.<br />
      Currently: <code>{{ props.columns }}</code>, <code>{{ props.align }}</code>, <code>{{ props.color }}</code>, <code>{{ props.titlepos }}</code>.
    </p>
    <p>
      The <code>columns</code> param divides the 12-grid into left, center, right columns (e.g. <code>is-4-4-4</code>).
      You can also shorthand (<code>is-one-third</code> = <code>is-4-4-4</code>).
    </p>
    <p>
      <code>align</code> controls horizontal/vertical alignment for each region — e.g. <code>align: c-lt-ct-rt</code>.
    </p>
  </div>

  <div v-else class="slidecolor" :class="flexclass + ' ' + colorscheme">
    <div v-if="$slots.title && props.titlepos != 'n'" class="title" :class="alignment.t">
      <slot name="title" />
    </div>

    <div v-if="$slots.left" class="left-col" :class="alignment.l">
      <slot name="left" />
    </div>

    <div v-if="$slots.center" class="center-col" :class="alignment.c">
      <slot name="center" />
    </div>

    <div v-if="$slots.right" class="right-col" :class="alignment.r">
      <slot name="right" />
    </div>

    <div v-if="$slots.default" class="end">
      <slot name="default" />
    </div>
  </div>
</template>

<style>
/* ─────────────── GRID STRUCTURE ─────────────── */
.slidev-layout.three-cols,
.slidev-layout.three-cols-header,
.slidev-layout.three-cols-footer {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-auto-rows: auto;
}

.slidev-layout.three-cols-header {
  grid-template-rows: auto 1fr auto;
}
.slidev-layout.three-cols-footer {
  grid-template-rows: 1fr auto auto;
}

/* ─────────────── TITLE AREA ─────────────── */
.slidev-layout.three-cols-header .title {
  grid-area: 1 / 1 / 2 / span 12;
  margin-bottom: 1rem;
}
.slidev-layout.three-cols-footer .title {
  grid-area: 3 / 1 / 4 / span 12;
  margin-top: 1rem;
}
.slidev-layout.three-cols .title h1 + p,
.slidev-layout.three-cols-header .title h1 + p,
.slidev-layout.three-cols-footer .title h1 + p {
  margin-top: 0.1em;
  margin-bottom: 0;
}

/* ─────────────── CONTENT COLUMNS ─────────────── */
.slidev-layout.three-cols .left-col,
.slidev-layout.three-cols-header .left-col,
.slidev-layout.three-cols-footer .left-col,
.slidev-layout.three-cols .center-col,
.slidev-layout.three-cols-header .center-col,
.slidev-layout.three-cols-footer .center-col,
.slidev-layout.three-cols .right-col,
.slidev-layout.three-cols-header .right-col,
.slidev-layout.three-cols-footer .right-col {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

/* ─────────────── END SLOT ─────────────── */
.slidev-layout.three-cols .end,
.slidev-layout.three-cols-header .end,
.slidev-layout.three-cols-footer .end {
  grid-column: 1 / span 12;
  margin-top: 1rem;
}
</style>

<style scoped>
/* scoped column placement based on computed v-bind */
.three-cols .left-col,
.three-cols-header .left-col,
.three-cols-footer .left-col {
  grid-area: 2 / 1 / 3 / span v-bind(colwidth.l);
}

.three-cols .center-col,
.three-cols-header .center-col,
.three-cols-footer .center-col {
  grid-area: 2 / v-bind(colwidth.l + 1) / 3 / span v-bind(colwidth.c);
}

.three-cols .right-col,
.three-cols-header .right-col,
.three-cols-footer .right-col {
  grid-area: 2 / v-bind(colwidth.l + colwidth.c + 1) / 3 / span v-bind(colwidth.r);
}
</style>
