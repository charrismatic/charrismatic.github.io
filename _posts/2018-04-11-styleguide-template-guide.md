---
layout: post
categories: ['code']
tags: [ 'github-gist', 'codepen', 'styleguide', 'frontend', 'design']
title: Styleguide Template Guide
---

I created an simple single-page styleguide Styleguide Templates to get started with theming and/or documenting your styles.

The main goal of this project was to find a way that a set of color patterns and fonts could be generated very quickly without needing to change too many things from one project to the next.

Each page follows the same basic principles

  - There is a light variation and an inverse dark variation.
  - Each set of colors has a base color, plus a lighter, and darker variation.
  - Besides from light and dark, there are also full-color designs
  - For each full-color theme there is
    - a variation with only white or black typography
    - a variation that uses the theme color for the text that uses the darkest and lightest color variation to produce good contrast.

In the example below I only choose 3 colors to test with but this produced 6 theme templates in the end.

Each of the themes only needs to be set with a single css class at the main section container for each page as well.

This was my first attempt at automating themes and styleguide. For a more advanced version of this see [charrismatic/hugo-styleguider](https://github.com/charrismatic/hugo-styleguider)


---

A [Pen](https://codepen.io/super_thalamus/pen/Bdzzxx) by [Matt Harris](https://codepen.io/super_thalamus) on [CodePen](https://codepen.io).


<p class="codepen" data-height="528" data-theme-id="light" data-default-tab="result" data-user="super_thalamus" data-slug-hash="Bdzzxx" style="height: 528px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="Styleguide Template Template">
  <span>See the Pen <a href="https://codepen.io/super_thalamus/pen/Bdzzxx/">
  Styleguide Template Template</a> by Matt Harris (<a href="https://codepen.io/super_thalamus">@super_thalamus</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

---

Source

{% gist charrismatic/cb28e5daf99d6c9ef13360d3318479b8 %}
