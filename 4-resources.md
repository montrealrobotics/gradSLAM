---
title: Resources
nav: true
---

# Resources

To learn how to use `workshop-template`, the [Readme]({{ "README.md" | absolute_url }}) and content pages have some documentation.

Other workshop sites using this template:

- [get-git](https://evanwill.github.io/get-git/)
- [hello-arduino](https://evanwill.github.io/hello-arduino/)
- [clean-your-data](https://evanwill.github.io/clean-your-data/)
- [go-go gh-pages](https://evanwill.github.io/go-go-ghpages/)
- [Make @ the MILL](https://uidaholib.github.io/make-at-the-mill/)

# Reference

### Git & GitHub

[GitHub](https://github.com/){:target="_blank"} is a popular web service for hosting Git repositories--with benefits!
It provides a handy web interface for editing and collaborating on repos, as well as, built in project management features and static web hosting.
Accounts are free for public repositories--private repositories are available on a subscription pricing model.
To learn more check out Hellow World on [GitHub Guides](https://guides.github.com/){:target="_blank"} or [GitHub Training](https://services.github.com/on-demand/){:target="_blank"}.

### Markdown

[Markdown](https://daringfireball.net/projects/markdown/) is a standard to simplify writing content for the web. 
[GitHub markdown flavor](https://help.github.com/articles/basic-writing-and-formatting-syntax/) can be used any where on GitHub and in Jekyll.

- [Markdown in a Minute](https://evanwill.github.io/_drafts/notes/markdown-minute.html)
- GitHub Guide [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

### YAML

[YAML](http://www.yaml.org/) is a human readable plain text data format.
It is used in Jekyll for configuration, site data, and front matter.
Jekyll projects are [configured](https://jekyllrb.com/docs/configuration/) using the `_config.yml` file.

### Liquid

[Liquid](http://shopify.github.io/liquid/) is a flexible template language.
[In Jekyll](https://jekyllrb.com/docs/templates/) it allows you to layout pages built from modular components and data, using the `_includes`, `_layouts`, and `_data` directories.
Liquid includes features such as operators, loops, and filters to manipulate raw content. 
Liquid statements are enclosed by {% raw %}`{%  %}`{% endraw %} and variables in {% raw %}`{{  }}`{% endraw %}.

### Sass  

[Sass](http://sass-lang.com/) is a CSS extension / preprocessor. 
All normal CSS is valid SCSS, but Sass adds many powerful functions and programatic features. 
Writing SCSS is often easier and more sensible, for example by supporting nesting, variables, and operators. 
Jekyll lets you write SASS in modular chucks called partials, in the `_sass` directory, that will be combined and compiled into normal CSS files when the site is built.
