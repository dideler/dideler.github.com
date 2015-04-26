My personal website.

- Install dependencies with `bundle install`
- Update dependencies (such as Jekyll) with `bundle update`
- Preview site with `rake site:preview` (opens a browser tab)
- Create a post with `rake post:new[title]`

If a post doesn't have it's own cover image, it uses the site's cover image.

You can use YAML front-matter to load custom CSS and JS for a page. E.g.
```
---
custom_css: foobar
custom_js:
- jquery.min
- foobar
---
```

----

Built on top of the [Thinny Jekyll theme](https://github.com/camporez/Thinny),
[v2.1](http://camporez.com/blog/hello-cosette/).

Powered by [GitHub Pages](https://pages.github.com/).
