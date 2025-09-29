---
# try also 'default' to start simple
theme: neversink
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Dataerai
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# Dataerai

<!-- Guarding Knowledge. Enabling Trust. Unlocking Innovation. -->
The commune where research data fuels breakthroughs.

<div @click="$slidev.nav.next" class="mt-10 py-1 text-sm" hover:bg="white op-10">
  Explore the <code>space</code> of Dataerai <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: two-cols-title
---

::title::
# Traction — Regulatory Tailwinds

::left::

### Regulatory Tailwinds

- **Mandates are here:** NIH DMS (2023) + OSTP (2022→2025) push open, preserved, AI-ready data.
- **Risk is rising:** 
- **Funding aligns:** Data rigor now factors into awards/renewals.
- **Market timing:** Universities want a third-party data management solution --> an accountable standard solution.
- **Data → AI pull:** Curated, permissioned datasets provides research and industry innovation through Data Analytics and AI.

::right::

### Early Signals

- All agencies NSF, NIH, DARPA, DOE, DOD have programs to improve data management
- Collaborators at Stanford, University of Washington, Berkeley, Fermi Labs, Oak Ridge National Laboratory, and more have used DataFed, the open-source foundation of Dataerai
- More than 300 active users of software stack --> requires home-built hardware implementation and policy development

> **We turn regulatory lift into an AI elevator.**
