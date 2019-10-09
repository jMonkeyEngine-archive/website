a [gohugo.io](https://gohugo.io) website for the jmonkeyengine.org website.

These files are the content and theme files used to generate flat html files using gohugo.

To use these files:
* Download [gohugo.io](https://gohugo.io/getting-started/installing/).
* execute `git clone https://github.com/jMonkeyEngine/website.git` in the directory containing hugo.
* navigate into the `website` directory created by the clone action.
* execute the `hugo` command to compile the files to flat HTML. These files are compiled to the `./public` directory.
* execute `hugo server -D` to start a server on localhost:1313 and allow live-editing of the files.

Executing the `hugo` command will compile and publish all files into the `./public` folder.

### Updating the main website

The `./website/public` directory contains a git repository pointing to https://github.com/jMonkeyEngine/jmonkeyengine-ghpage. This repository contains the content that is displayed on the jmonkeyengine.org domain.

- Carry out any changes you wish to make.
- Execute the `hugo` command in the `website` directory to build the static pages to the `public` directory.
- Navigate to the `./website/public/` directory.
- Commit and Push your changes.

### Creating News Pages

To create a new blog page, create a new markdown file in the `./website/content/blog/` directory named `somename.md` and use the template below.

``` markdown
---
title: "The Title of My Article"
date: 2019-10-08T06:27:00+00:00
draft: false
type: "blog"
layout: "post"

authors:
    - "jayfella"

tags:
    - "asset-store"
    - "software"
---

This is my article. There are many like it but this one is mine.

![A small image](https://i.imgur.com/YsbKHg1.gif)

{{< figure
    src="//i.ibb.co/42rX9bm/image.png"
    class="ui fluid image"
    title="A large image that needs to be resized based on the width of the window."
>}}

My article is my best friend. It is my life. I must master it as I must master my life.

```

