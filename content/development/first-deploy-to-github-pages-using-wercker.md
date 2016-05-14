+++
Categories = ["development", "wercker"]
Description = ""
Tags = ["development", "wercker", "github pages", "issue"]
date = "2016-05-15T00:10:38+10:00"
title = "First deploy to Github Pages using Wercker"

+++

I've finally deployed this blog site to [Github Pages](https://pages.github.com/) using [Wercker](http://wercker.com/) (which means any new things I add will be available on the blog site in no time). The url to this blog site is http://www.dyliew.com/blog.

However, it took me a few hours to successfully do this. My first attempt was a failure as almost everything was deployed the my repository's _gh-pages_ branch but things in the _static_ folder (e.g. _css_, _js_ and _fonts_). It annoyed me a lot and I thought I did follow everything written in the [instruction](https://gohugo.io/tutorials/automated-deployments/).

I took a short break and created an exact copy of what have written in the instruction. After reconfiguring everything from GitHub to Wercker, everything worked for the copy and then I noticed something. I might have missed this
```
echo "User-agent: *\nDisallow:" > static/robots.txt
```
and I forgot to remove _.git_ folder in the theme I cloned.

I then removed everything related to the blog site from GitHub and Wercker and restarted the process from scratch. Finally, it worked!

I have a lot of todos in this blog site like setting up __https__ and proper __404__ page, __tags__, __categories__, __search__, etc. Hopefully I will be really motivated to do them in my free time.