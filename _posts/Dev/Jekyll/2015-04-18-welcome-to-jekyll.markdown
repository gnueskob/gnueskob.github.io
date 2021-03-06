---
layout: post
title:  "Welcome to Jekyll!"
date:   2015-04-18 08:43:59 +0900
author: Ben Centra
categories: jekyll
tags: jekyll makrdown
cover:  "/assets/instacode.png"
---

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

## Adding New Posts

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

### Tags and Categories

If you list one or more categories or tags in the front matter of your post, they will be included with the post on the page as links. Clicking the link will bring you to an auto-generated archive page for the category or tag, created using the [jekyll-archive][jekyll-archive] gem.

### Cover Images

To add a cover image to your post, set the "cover" property in the front matter with the relative URL of the image (i.e. `cover: "/assets/cover_image.jpg"`).

### Code Snippets

You can use [highlight.js][highlight] to add syntax highlight code snippets:

Use the [Liquid][liquid] `{% raw %}{% highlight <language> %}{% endraw %}` tag to add syntax highlighting to code snippets.

For instance, this template...

{% highlight text %}
{% raw %}{% highlight javascript %}
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
{% endhighlight %}{% endraw %}
{% endhighlight %}

...will come out looking like this:

{% highlight javascript %}
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
{% endhighlight %}

Syntax highlighting is done using [highlight.js][highlight]. You can change the active theme in [head.html](https://github.com/bencentra/centrarium/blob/2dcd73d09e104c3798202b0e14c1db9fa6e77bc7/_includes/head.html#L15).

***

- 2019-07-14 Add

추가로, markdown에서 제공하는 `Fenced Code Block` template를 이용할 수도 있음

하지만 빌드 시 제대로 적용되지 않는 언어들도 존재하거나 indention도 달라지므로 가능하면 `Liquid` 사용을 권장

{% highlight text %}

```js
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
```

{% endhighlight %}

```js
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
```

***

### Images

Lightbox has been enabled for images. To create the link that'll launch the lightbox, add `data-lightbox` and `data-title` attributes to an `<a>` tag around your `<img>` tag. The result is:

<!-- markdownlint-disable MD033 -->
```html
<a href="//bencentra.com/assets/images/falcon9_large.jpg" data-lightbox="falcon9-large" data-title="Check out the Falcon 9 from SpaceX">
  <img src="//bencentra.com/assets/images/falcon9_small.jpg" title="Check out the Falcon 9 from SpaceX">
</a>
```

<a href="//bencentra.com/assets/images/falcon9_large.jpg" data-lightbox="falcon9-large" data-title="Check out the Falcon 9 from SpaceX">
  <img src="//bencentra.com/assets/images/falcon9_small.jpg" title="Check out the Falcon 9 from SpaceX">
</a>

For more information, check out the [Lightbox][lightbox] website.

***

- 2019-07-14 Add

markdown template을 이용하는 경우 `{: attribute="value" }`를 통해 추가 가능

```md
# one line
[

  ![img]({{"/assets/imgs/2.jpg"}})  <= md image template
  {: title="bonobono" style="max-width: 50%; height: auto;" }   <= additional attribute

]({{"/assets/imgs/2.jpg"}})   <= md link template
{: data-lightbox="falcon9-large" data-title="real size bonobono" }  <= additional attribute
```

[![img]({{"/assets/imgs/2.jpg"}}){: title="bonobono" style="max-width: 50%; height: auto;" }]({{"/assets/imgs/2.jpg"}}){: data-lightbox="falcon9-large" data-title="real size bonobono" }

***

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[highlight]:   https://highlightjs.org/
[lightbox]:    http://lokeshdhakar.com/projects/lightbox2/
[jekyll-archive]: https://github.com/jekyll/jekyll-archives
[liquid]: https://github.com/Shopify/liquid/wiki/Liquid-for-Designers
