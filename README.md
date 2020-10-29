# liquify
A Jekyll plugin that Liquid parses the input.

## Use Case
I created this small plugin for my project as a quick-fix for one of (many) Liquid's glaring holes. I discovered that Liquid does not parse its contents recursively, that is, it will parse `{{ description }}` or `{% include file.md %}` and replace it by its contents, but it will not parse the contents itself for any Liquid tags.

This is quite similar to the `markdownify` filter, since Liquid also does not parse markdown in an included markdown file. This can be solved by the [markdown](https://gist.github.com/tmtk75/1408402) plugin or the `markdownify` filter included in Jekyll. [This post](https://web.archive.org/web/20150402090957/http://wolfslittlestore.be/2013/10/rendering-markdown-in-jekyll) elaborates it further.

## Installation
To install the plugin, simply put it in a folder named **_plugins** in your jekyll project directory.

## Usage
    {{ description | liquify }}
