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

<div class="emphasis">We turn regulatory lift into an AI elevator.</div>

::title::
# Traction

::left::
## Regulatory Tailwinds
- **Mandates are here:** NIH DMS (2023) + OSTP (2022→2025) push open, preserved, AI-ready data.
- **Risk is rising:** AI agents are increasingly being used to detect errors and fraud in R&D data.
- **Funding aligns:** Data availability is now a funding criterion—turn compliance into a grant advantage.
- **Market timing:** Universities want a third-party data management solution --> an accountable standard solution.
- **Data → AI pull:** Curated, permissioned datasets fuel research and industry innovation through data analytics and AI.

::right::

## Early Signals
- Major funding agencies — NSF, NIH, DARPA, DOE, and DoD — are all launching initiatives to strengthen research data management and sharing requirements.
- Collaborators at Stanford, the University of Washington, UC Berkeley, Fermi Lab, Oak Ridge National Laboratory, and others have adopted **DataFed**, the open-source foundation of **Dataerai**.
- Over **300 active users** currently rely on this software stack. However, the existing open-source implementation demands custom hardware builds and extensive policy development — a heavy lift for understaffed IT teams often at odds with researchers.

---
layout: side-title
side: l
color: violet
titlewidth: is-4
align: rm-lm
---

:: title ::

# `National Science Foundation`
<div class="flex justify-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/NSF_logo.png" alt="NSF Logo" style="height: 80px; margin-bottom: 1rem;" />
</div>

# <mdi-arrow-right />

:: content ::

## Data Retention

<a href="https://www.nsf.gov/funding/data-management-plan" target="_blank" rel="noopener" style="display: inline-block; padding: 0.5em 1.2em; background: #8b5cf6; color: #ede9fe; border-radius: 0.4em; text-decoration: none; font-weight: bold; margin: 0.5em 0;">
  Minimum data retention of research data is three years after the conclusion of the award or three years after public release, whichever is later.
</a>

## Data Sharing

<a href="https://www.nsf.gov/funding/data-management-plan" target="_blank" rel="noopener" style="display: inline-block; padding: 0.5em 1.2em; background: #8b5cf6; color: #ede9fe; border-radius: 0.4em; text-decoration: none; margin: 0.5em 0;">
  NSF-funded investigators are expected to share with other researchers, at no more than incremental cost and within a reasonable time, the primary data, samples, physical collections and other supporting materials created or gathered in the course of work under NSF awards.
</a>

---
layout: side-title
side: l
color: emerald
titlewidth: is-4
align: rm-lm
---

:: title ::

# `National Institutes of Health`
<div class="flex justify-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/a/a6/NIH_2013_logo_vertical.svg" alt="NIH Logo" style="height: 80px; margin-bottom: 1rem;" />
</div>

# <mdi-arrow-right />

:: content ::

## Data Retention

<a href="https://grants.nih.gov/grants/policy/nihgps/html5/section_8/8.4.2_record_retention_and_access.htm" target="_blank" rel="noopener" style="display: inline-block; padding: 0.5em 1.2em; background: #10b981; color: #f0fdf4; border-radius: 0.4em; text-decoration: none; margin: 0.5em 0;">
Recipients generally must retain financial and programmatic records, supporting documents, statistical records, and all other records that are required by the terms of a grant, or may reasonably be considered pertinent to a grant, for a period of 3 years from the date the annual FFR is submitted.
</a>

## Data Sharing

<a href="https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/dms/policy-overview" target="_blank" rel="noopener" style="display: inline-block; padding: 0.5em 1.2em; background: #10b981; color: #f0fdf4; border-radius: 0.4em; text-decoration: none; margin: 0.5em 0;">
  NIH expects that data be made as widely and freely available as possible while safeguarding the privacy of participants and protecting confidential and proprietary data. Sharing is particularly important for unique data that cannot be readily replicated.
</a>

---
layout: side-title
side: l
color: indigo
titlewidth: is-4
align: rm-lm
title: Side Title Layout (Another)
---

:: title ::

# `Department of Energy`
<div class="flex justify-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Seal_of_the_Department_of_Energy.svg" alt="DOE Logo" style="height: 80px; margin-bottom: 1rem;" />
</div>

# <mdi-arrow-right />

:: content ::

## Data Retention

<a href="https://www.law.cornell.edu/cfr/text/10/600.153#:~:text=10%20CFR%20%C2%A7%20600.153%20sets%20forth%20requirements,requirement%20does%20not%20apply%20to%20the%20recipient." target="_blank" rel="noopener" style="display: inline-block; padding: 0.5em 1.2em; background: #6366f1; color: #f0fdf4; border-radius: 0.4em; text-decoration: none; margin: 0.5em 0;">
Financial records, supporting documents, statistical records, and all other records pertinent to an award shall be retained for a period of three years from the date of submission of the final expenditure report or, for awards that are renewed quarterly or annually, from the date of the submission of the quarterly or annual financial report, as authorized by DOE. 
</a>

## Data Sharing

<a href="https://grants.nih.gov/policy-and-compliance/policy-topics/sharing-policies/dms/policy-overview" target="_blank" rel="noopener" style="display: inline-block; padding: 0.5em 1.2em; background: #6366f1; color: #f0fdf4; border-radius: 0.4em; text-decoration: none; margin: 0.5em 0;">
  <ul>
    <li>Provide free, immediate access to peer-reviewed, scholarly publications</li>
    <li>Provide immediate access to scientific data displayed in or underlying publications and increased access to other data</li>
    <li>Use persistent identifiers (PIDs) for research outputs, researchers, organizations, and awards</li>
  </ul>
</a>

---
layout: ncolumns
titleText: "DataFed Infrastructure"
columns: 2
images:
- facilities/lehigh-cluster.png
- null
  titles:
- null
- "Ideal Computational Infrastructure"
  titleClicks: [0, 1]
  columnWidths: [1.5, 2]
  textboxHeight: 0
  mainHeight: 75
---

<template #col0>
**DataFed** is a federated research data management platform.
</template>

<template #col1>

<div v-click="1"  class="flex flex-col h-full">
  <div v-click="1" class="text-left gap-4 flex-1">
    <ul class="list-disc pl-4">
      <li>Distributed storage across facilities</li> 
      <li>At least moderate performance</li>
      <li>Globus Connect Server</li>
      <li>Open ports 50000-51000</li>
    </ul>
  </div>
  <div v-click="2" class="flex-1 flex justify-center items-center">
    <div class="flex flex-col items-center">
      <img src="" class="h-[100px] object-contain" alt="Lehigh Cluster" />
      <h3>StorJ</h3>
    </div>
  </div>
</div>

</template>

<style>
ul li {
  line-height: .9;
  margin-bottom: 0.2em;  /* Remove margin at the bottom of list items */
  padding-bottom: 0.2em;  /* Remove padding at the bottom of list items */
}
p {
  margin-top: 0.1em;
  margin-bottom: 0.1em;
}

.emphasis {
  text-align: center;
  font-weight: bold;
  border: 2px solid currentColor;
  padding: 1rem 2rem;
  margin: 1rem auto;
  max-width: fit-content;
}
</style>
