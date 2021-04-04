---
layout: page
title: Style Guide
permalink: /styleguide/
image: '/images/81.jpg'
---

A paragraph looks like this — Haec et tu ita posuisti, et verba vestra sunt. Idemne potest esse dies saepius, qui semel fuit? Ampulla enim sit necne sit, quis non iure optimo irrideatur, silaboret? Ego vero volo in virtute vim esse quam maximam; Serpere anguiculos, nare anaticulas, evolare merulas, cornibus uti videmus boves, nepas aculeis. Conferam tecum, quam cuique verso rem subicias; Si longus, levis. In qua quid est boni praeter summam voluptatem, et eam cur post. Tarentum ad Archytam? Qua ex cognitione facilior facta est investigatio rerum occultissimarum. Natura sic ab iis investigata est, ut nulla pars caelo deinde optimum.

***

## Headings by default:

# H1 For example
## H2 For example
### H3 For example
#### H4 For example
##### H5 For example
###### H6 For example

{% highlight markdown %}
## Heading first level
### Heading second level
#### Heading third level
{% endhighlight %}

***

## Lists

#### Ordered list example:

1. Poutine drinking vinegar bitters.
2. Coloring book distillery fanny pack.
3. Venmo biodiesel gentrify enamel pin meditation.
4. Jean shorts shaman listicle pickled portland.
5. Salvia mumblecore brunch iPhone migas.

{% highlight markdown %}
1. Order list item 1
2. Order list item 1
{% endhighlight %}

***

#### Unordered list example:

* Bitters semiotics vice thundercats synth.
* Literally cred narwhal bitters wayfarers.
* Kale chips chartreuse paleo tbh street art marfa.
* Mlkshk polaroid sriracha brooklyn.
* Pug you probably haven't heard of them air plant man bun.

{% highlight markdown %}
* Unordered list item 1
* Unordered list item 2
{% endhighlight %}

***

### Table

<div class="table-container">
  <table>
    <tr><th>Header 1</th><th>Header 2</th><th>Header 3</th><th>Header 4</th><th>Header 5</th></tr>
    <tr><td>Row:1 Cell:1</td><td>Row:1 Cell:2</td><td>Row:1 Cell:3</td><td>Row:1 Cell:4</td><td>Row:1 Cell:5</td></tr>
    <tr><td>Row:2 Cell:1</td><td>Row:2 Cell:2</td><td>Row:2 Cell:3</td><td>Row:2 Cell:4</td><td>Row:2 Cell:5</td></tr>
    <tr><td>Row:3 Cell:1</td><td>Row:3 Cell:2</td><td>Row:3 Cell:3</td><td>Row:3 Cell:4</td><td>Row:3 Cell:5</td></tr>
    <tr><td>Row:4 Cell:1</td><td>Row:4 Cell:2</td><td>Row:4 Cell:3</td><td>Row:4 Cell:4</td><td>Row:4 Cell:5</td></tr>
    <tr><td>Row:5 Cell:1</td><td>Row:5 Cell:2</td><td>Row:5 Cell:3</td><td>Row:5 Cell:4</td><td>Row:5 Cell:5</td></tr>
    <tr><td>Row:6 Cell:1</td><td>Row:6 Cell:2</td><td>Row:6 Cell:3</td><td>Row:6 Cell:4</td><td>Row:6 Cell:5</td></tr>
  </table>
</div>

***

## Quotes

#### A quote looks like this:

> The longer I live, the more I realize that I am never wrong about anything, and that all the pains I have so humbly taken to verify my notions have only wasted my time!
>
> <cite>George Bernard Shaw</cite>

{% highlight html %}
> The longer I live, the more I realize that I am never wrong about anything, and that all the pains I have so humbly taken to verify my notions have only wasted my time!
>
> <cite>George Bernard Shaw</cite>
{% endhighlight %}

***



## Syntax Highlighter

{% highlight js %}
  $('.top').click(function () {
    $('html, body').stop().animate({ scrollTop: 0 }, 'slow', 'swing');
  });
  $(window).scroll(function () {
    if ($(this).scrollTop() > $(window).height()) {
      $('.top').addClass("top-active");
    } else {
      $('.top').removeClass("top-active");
    };
  });
{% endhighlight %}

***

## Images

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/51.jpg">
    <img src="/images/52.jpg">
    <img src="/images/63.jpg">
    <img src="/images/54.jpg">
    <img src="/images/68.jpg">
    <img src="/images/56.jpg">
  </div>
  <em>Gallery / <a href="https://unsplash.com/" target="_blank">Unsplash</a></em>
</div>

{% highlight markdown %}
  <div class="gallery-box">
    <div class="gallery">
      <img src="/images/51.jpg">
      <img src="/images/52.jpg">
      <img src="/images/63.jpg">
      <img src="/images/54.jpg">
      <img src="/images/68.jpg">
      <img src="/images/56.jpg">
    </div>
    <em>Gallery / <a href="https://unsplash.com/" target="_blank">Unsplash</a></em>
  </div>
{% endhighlight %}

![]({{site.baseurl}}/images/41.jpg)
*Mountains*

{% highlight markdown %}
  ![]({{site.baseurl}}/images/41.jpg)
  *Mountains*
{% endhighlight %}

***

## Youtube Embed

<p><iframe src="https://www.youtube.com/embed/wB_KtOjm4IA" frameborder="0" allowfullscreen></iframe></p>

{% highlight html %}
  <iframe src="https://www.youtube.com/embed/wB_KtOjm4IA" frameborder="0" allowfullscreen></iframe>
{% endhighlight %}

## Vimeo Embed

<p><iframe src="https://player.vimeo.com/video/107654760" width="640" height="360" frameborder="0" allowfullscreen></iframe></p>

{% highlight html %}
  <iframe src="https://player.vimeo.com/video/107654760" width="640" height="360" frameborder="0" allowfullscreen></iframe>
{% endhighlight %}

***