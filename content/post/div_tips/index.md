---

title: How to Make Custom Note Boxes for MD Files?
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
featured: 'featured.jpg'
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


A few months ago, I started to learn how to create a blog using R Markdown from scracth. Initially, I knew very little about Markdown, and I had absolutely no idea about HTML or CSS. Right after launching my own blog, I came across with the [**bookdown website of Yihui**](https://bookdown.org/yihui/blogdown/output-format.html) and saw some really cute colorful boxes there. It seemed like a great way to highlight important information, so I started searching for the code of these colorful boxes.



<style>
div.yellow {
    background-image: url("note.png");
}
</style>

<div class = "yellow">
An example note box.
</div>

Then, I found the [**website of Desirée de Leon**](https://desiree.rbind.io/post/2019/making-tip-boxes-with-bookdown-and-rmarkdown/). I recommend that you check it out on her website as well. She mentions that these div tips don't work on blogdown <mark> .md </mark> posts; but I'm quite stubborn and I really liked these so I struggled for a few days trying to make it work.

&nbsp;


## Steps for Creating the Custom Boxes

Most of the steps will be the same with Desirée's but we'll take some additional steps while using the colorful boxes in our blog posts to make it compatible with <mark> .md </mark> extensions.

First of all, you will need to create a CSS file if you do not already have it. If you are using blogdown with Hugo Academic theme, you need to follow the steps [**over here**](https://wowchemy.com/docs/customization/). All you need to do is;
 
 - Create an <mark>assets/scss/</mark> file in your root directory. 
 - Create a <mark>custom.scss</mark> file on your scss folder.
 
So far so good.

Now we will add our custom div tips to the custom.scss file. Go ahead and paste the CSS below into your file.

```r

/* Div Tips */

div.yellow { 
  background-color: #FEF5E7; padding: 1em;
  margin: 1em 0;
  padding-left: 100px;
  background-size: 70px;
  background-repeat: no-repeat;
  background-position: 15px center;
  min-height: 120px;
  border: solid 2px #FAD7A0;
  }

```
I named this box as <mark>yellow</mark> (see the word after 'div.') so that I can easily remember and find the yellow box CSS when I need to. You can change the name however you like. Accordingly, you may create as many different div tips as you like by changing the properties above. Make sure that you give each one a unique name as we will be using those later on.

&nbsp;


## How to Customise the Boxes


![](example.jpg)

Especially four lines in our CSS will come in handy while customising our boxes. These are;

- <mark>background-image:</mark> which we will be learning how to use in a minute.
- <mark>border:</mark> you can set this property to dotted, dashed, solid and so on. Check your other options [**here**](https://www.w3schools.com/css/css_border.asp). You can also change the thickness (2px) and color with this one (#FAD7A0).
- <mark>color:</mark> This spesifically refers to the color of your text. 
- <mark>background-color:</mark> You can use any color of your liking, both HTML and RGB color codes work.

&nbsp;


## The Background Image

This is where our paths are seperated with Dr. Desirée. If you, for whatever reason, couldn't add your icon in the box, try these steps instead;

- Choose an [**icon**](https://www.flaticon.com) of your liking and save it as png or jpg format (make sure that it has a transparent background).
- Add this image in the same file as your .md blog post.
- Open up your blog post and paste this CSS

```r
div.yellow {
  background-image: url("your_icon_name.png");
}
```