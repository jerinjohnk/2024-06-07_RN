---
# try also 'default' to start simple
theme: dracula
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
# some information about your slides, markdown enabled
title: Welcome to React Native Workshop
info: |
  Learn to build Mobile Applications using React Native
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
hideInToc: true
favicon: './favicon.ico'
---

# Welcome to React Native Workshop

Learn to build mobile application using react native.

<div class="abs-br m-6 flex gap-2">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer"
    hover="bg-white bg-opacity-10">
    Speakers <carbon:bullhorn class="inline"/>
  </span>
 <span class="px-2 py-1 rounded">
    Jerin
  </span>
  <span class="px-2 py-1 rounded">
    Shailesh
  </span>
  <span class="px-2 py-1 rounded">
    Prerna
  </span>
</div>

<!--
Title Page
-->

---
layoutClass: gap-16
hideInToc: true
---

# Table of contents

<Transform :scale="0.8">
  <Toc minDepth="1" maxDepth="2" columns="2"></Toc>
</Transform>

<!--
Table of contents
-->

---
src: ./pages/rn.md
---
