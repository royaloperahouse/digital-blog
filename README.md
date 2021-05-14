# ROH Digital blog

A blog about digital projects at the Royal Opera House, administered as a [Hugo](https://gohugo.io/) site hosted in [GitHub Pages](https://pages.github.com/).

## Publishing notes

You can use the [editor on GitHub](https://github.com/royaloperahouse/royaloperahouse.github.io/edit/main/README.md) to maintain and preview the content of the site in [Markdown](https://guides.github.com/features/mastering-markdown/) files.

To create a new post, make a new file in `content/posts/`, e.g. `title-of-post.md`. The top of the file contains the meta-data, e.g.

```
---
title: "Five design principles"
slug: "five-design-principles"
date: 2021-05-11T10:41:49+01:00
authors: ["Tom Dyson"]
draft: false
tags:
- architecture
- systems
- digital stage
---
```

(only `title`, `slug` and `date` are necessary).

The [live site](https://royaloperahouse.github.io/) is automatically updated when you make changes in GitHub.

### Adding images

1. In GitHub, upload the image file in the `static/images` folder.
2. Reference the image with the correct path and file name from your post: `![Image alt text](/images/my-file-name.png)`.

### Preview locally

[Install Hugo](https://gohugo.io/getting-started/installing/), then:

```
hugo serve -D
```

### Edit the theme

```bash
cd /themes/hugo-tailwind-journal-master
yarn watch
```