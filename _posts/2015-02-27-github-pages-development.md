---
layout: post
title: github pages development
excerpt: Edit and view your site instantly by generating it locally using this docker image.
---
{{ page.excerpt }}


When I write software I like to edit and run.
For the blog I wanted to edit and browse.
Github pages are great.
But I was getting tired of edit, commit, push, wait, browse.
Running the jekyll server is the answer, it listens to the file system changes for your site source code and instantly re-generates the site.

But that is a lot of work to set up, right?
Not really.
Install docker on your linux computer.
Use this docker image: powellquiring/jekyllgithubpages

Then use this alias to start the jekyll server:


{% highlight bash %}
$ docker pull powellquiring/jekyllgithubpages
$ alias jekyll='sudo docker run --rm -v "$PWD:/src" -p 4000:4000 powellquiring/jekyllgithubpages serve -H 0.0.0.0'
$ cd gitRepoForMySite
$ jekyll
{% endhighlight %}

The jekyll server listens to the file system changes (.i.e your edits) and regenerates the _site the instant you write the file from the editor.
Edit and browse.

To learn how to [create a docker image](/2015/03/02/create-a-docker-image/)
