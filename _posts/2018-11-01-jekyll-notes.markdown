---
layout: post
title:  "Jekyll Notes"
date:   2018-10-17 18:46:57 -0400
categories: jekyll update
---

{% highlight bash %}
=> bundle exec jekyll --build #bundle required to genererate rss feeds correctly
=> jekyll --serve
=> JEKYLL_ENV=production bundle exec jekyll clean
=> JEKYLL_ENV=production bundle exec jekyll build
=> s3_website push
{% endhighlight %}

~/.aws/credentials file required

https://github.com/dhaskew/blog

I use the [S3 Website][s3_website] tool to automate the uploading of the site to s3.

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[s3_website]: https://github.com/laurilehmijoki/s3_website
[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
