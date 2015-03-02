---
layout: post
title: Creating a blog using github pages - development environment
excerpt: Using a docker image to turn the develpopment crank works great
---
{{ page.excerpt }}


Use this Dockerfile: xxx
Then use this alias to start the jekyll server:


{% highlight bash %}
$ alias jekyll=sudo docker run --rm -v "$PWD:/src" -p 4000:4000 powellquiring/jekyll serve -H 0.0.0.0
$ cd gitRepoForMySite
$ jekyll
{% endhighlight %}

Believe it or not the jekyll server listens to the edits that you make and regenerates the _site.
Edit and browse.
