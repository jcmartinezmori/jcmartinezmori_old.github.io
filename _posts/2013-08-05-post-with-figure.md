---
layout: post-light-feature
title: "Post with Figure"
description: "Examples and code for displaying images in posts."
math: yes
category: articles
tags: [sample post, images, test]
---

This is a post that uses a `figure`. It stacks these images and places a nice little caption below if you fill out `figcaption`.

### Single Image Figure

<figure>
	<img src="{{site.url}}/images/typewriter.jpg">
	<figcaption>Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</figcaption>
</figure>

<p>
\begin{align}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{align}
</p>

{% highlight html linenos %}
<figure>
	<img src="/images/image-filename-1.jpg">
	<figcaption>Caption describing these two images.</figcaption>
</figure>
{% endhighlight %}

{% highlight scss linenos %}

  li {
            display: block;
            float: none;
            font-size: $fs3;
            margin-bottom: $lh*2;
            position: relative;
            
            a {
                color: $link;
                position: relative;
                &:hover {
                    color: $accent;
                    @include transit;
                }
            }
    
            a:hover:before {
                color: $grey-light;
                font-family: $sans;
                position: absolute;
                margin-left: -70px;
                font-size: 40px;
                left: 0;
                top: -20px;
                text-align: center;
                @include transit;
            }
            
            a:before {
                color: $grey-light;
                position: absolute;
                margin-left: -70px;
                font-size: 60px;
                z-index: 10;
                top: -6px;

{% endhighlight %}