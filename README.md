# bibihub

# 哔哔Hub

### The blog theme you may fall in love with, coming to Hexo. [Fork GitHub](http://github.com/toadgg/bibihub)
![preview](http://raw.githubusercontent.com/toadgg/bibihub/gallery/preview.png "")

## Installation

### Install

``` bash
$ git clone https://github.com/toadgg/bibihub.git themes/bibihub
```

**bibihub requires Hexo 3.0 and above.**

### Enable

1. Rename `themes\bibihub\_config.yml.example` to `themes\bibihub\_config.yml`;
3. Copy `themes\bibihub\_source\*` into your hexo blog's directory `source`;
4. Then modify `theme` setting in `_config.yml` to `bibihub`.

### Update

``` bash
cd themes/bibihub
git pull
```

## Configuration

### Theme configuration example
```r
# Header
menu:
  Home: .
  Archives: archives
  Categories: categories # you need to add extra page to enable this, please see the config below.
  Tags: tags             # you need to add extra page to enable this, please see the config below.
  About: about

# Content
excerpt_link: Read More
fancybox: true

# Sidebar
sidebar: right
widgets:
- recent_posts
- category
- tag
- tagcloud
- archive
thumbnail: true

# Contacts
contacts:
  github: https://github.com/toadgg/bibihub
  twitter: '#'
  facebook: '#'
  dribbble: '#'
  rss: atom.xml

# Links
links:
  Hexo: http://hexo.io

# CDN
cdn: # You can choose "useso" instead of "google apis"(default).
# cdn: useso
# OR
# cdn:

# Comment
comment:
    disqus_shortname: bibihub # enter disqus shortname here
    duoshuo_shortname: # enter duoshuo shortname here
    youyan: # enter youyan uid here
    
# Miscellaneous
google_site_verification:
google_analytics:
baidu_analytics:
swiftype_install_key:
favicon: /images/favicon.png
twitter:
google_plus:
fb_admins:
fb_app_id:
```

- **excerpt_link** - Cooperate with `<!-- more -->` tag to show only part of the article in index pages.
- **fancybox** - Enable [Fancybox].
- **contacts** - Your social network links, RSS link, etc.
- **widgets** - Widgets displaying in sidebar.
- **thumbnail** - Whether to show post thumbnails in the sidebar and archive pages.
- **links** - Links displayed in the link widget.
- **google_analytics** - Google Analytics ID.
- **baidu_analytics** - Baidu Analytics ID.
- **swiftype_install_key** - Enable [Swiftype].
- **favicon** - Favicon path.

![swiftype search](http://raw.githubusercontent.com/toadgg/bibihub/gallery/swiftype.png "")

### Site configuration example
```r
# Site
title: Bibihub
subtitle:
description: Hexo theme - Bibihub
author: toadgg
author_title: 'Web Developer & Designer'
avatar: css/images/avatar.png
location: 'Beijing, China'
follow: https://github.com/toadgg/
email: # Your email (Used to show Gravatar).
language: zh-CN
timezone: Asia/Shanghai
since: 2016 # The start year showing in your copyright section.
keywords: Web,前端,JavaScript,html5,css3
...
```

- **author_title** - Title to your occupation.
- **avatar** - Your avatar image link.
- **location** - Where you live in.
- **keywords** - Your Site keywords.

### Post Thumbnail & Banner

You can add a thumbnail and a banner to each post by adding the following lines into your post source files' front-matter:
```r
title: Demo
date: 2015-01-01
...
# add those
thumbnail: http://example.com/thumbnail.jpg
banner: http://example.com/banner.jpg
```

### Post Description & Keywords
```r
title: Nginx vs Tomcat
# add those
description: 本教程介绍了如何配置Nginx作为反向代理服务器...
Keywords: nginx,tomcat
```
![description](http://raw.githubusercontent.com/toadgg/bibihub/gallery/description.png "")
![Keywords](http://raw.githubusercontent.com/toadgg/bibihub/gallery/keywords.png "")

### Custom Categories & Tags Pages

To enable custom categories page and tags page, just copy the `categories` folder and `tags` folder under your theme's `_source` foler into your site's `source` folder. Then edit theme's _config.yml and add the following lines: 
```r
title: Nginx vs Tomcat
# add those
tags:
  - nginx
  - tomcat
categories:
  - nginx
```

### Languages

English and Simplified Chinese are the default languages of the theme. You can add translations in the `languages` folder and change the default language in blog's `_config.yml`.

```r
language: zh-CN
```

### You Can Change Your Hexo Blog’s root directory scaffolds post.md to this

```r
---
title: {{ title }}
description: 本教程出自BiBiHub
date: {{ date }}
tags: [dev]
categories: [dev]
thumbnail: thumbnail_url
banner: banner_url
keywords: dev
---

{% blockquote BiBiHub http://www.bibihub.com/ 文章来自BiBiHub%}
本教程出自BiBiHub
{% endblockquote %}
```

## Features

### Profile Sidebar

A nice place to show yourself. You can add your own information in your site's `_config.yml`

![](http://raw.githubusercontent.com/toadgg/bibihub/gallery/profile.png "")

### Post Banner & Thumbnail

Thanks to [atika](https://github.com/atika), you can now add thumbnails and banners to every post to create better reading experience.

### Responsive Layout

Bibihub knows on what screen size you are browsering the website, and reorganize the layout to fit your device.

![responsive](http://raw.githubusercontent.com/toadgg/bibihub/gallery/responsive.png "")

### Custom Categories & Tags Pages

Get your categories and tags listed in single pages to make your blog more methodic.

### Fancybox

Bibihub uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)
```

### Sidebar

Bibihub provides 6 built-in widgets:

- recent_posts
- category
- archives
- tag
- tagcloud
- links

All of them are enabled by default. You can edit them in `widget` setting.

## Development

### Requirements

- [Grunt] 0.4+
- Hexo 3.0+

### Grunt tasks

- **default** - Download [Fancybox] and [Font Awesome].
- **fontawesome** - Only download [Font Awesome].
- **fancybox** - Only download [Fancybox].
- **clean** - Clean temporarily files and downloaded files.

### Thx [ppoffice](https://github.com/ppoffice) , Because this theme fork form [hexo-theme-icarus](http://github.com/ppoffice/hexo-theme-icarus) 

[Hexo]: http://zespia.tw/hexo/
[Fancybox]: http://fancyapps.com/fancybox/
[Swiftype]: http://swiftype.com/
[Font Awesome]: http://fontawesome.io/
[Grunt]: http://gruntjs.com/
