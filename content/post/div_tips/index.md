---

title: How to Make Cute Note Boxes for MD Files?
subtitle: Using the custom div tip method for the files with .md extention.
date: 2021-01-05
slug: how-to-make-note-boxes
categories:
- RStudio
tags:
- Div Tips
- RStudio
- CSS
authors: [admin]
lastmod: ''
featured: '/post/div_tips/featured.png'
output:
  blogdown::html_page:
    dev: svg
image:
  caption: ''
  focal_point: Center
  preview_only: true
projects: []

---

&nbsp;


A few months ago, I started to learn how to create a blog using R Markdown from scracth. Initially, I knew very little about Markdown, and I had absolutely no idea about HTML or CSS. Right after launching my own blog, I came across with the <a href = "https://datasciencebox.org/hello-world.html" bookdown website of Mine Çetinkaya-Rundel> and saw some really cute colorful boxes there. It seemed like a great way to highlight important information, so I started searching for the code of these colorful boxes.

<style>
div.yellow {
    background-image: url("note.png");
}
</style>

<div class = "yellow">
An example note box.
</div>