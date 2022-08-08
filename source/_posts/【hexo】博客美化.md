---
title: 【Hexo】博客美化
date: 2022-08-08 21:37:13
tags: Hexo
description: Hexo博客美化
---

## 1、博客个人信息配置

修改`_config.yml`配置文件

~~~bash
# Site
title: Oort. - PersonalBlogs
subtitle: 'Personal Blogs'
description: 'This is personal blogs for Oort.'
keywords:
author: Oort
language: zh-CN
timezone: 'Asia/Shanghai'
~~~

## 2、安装Next主题

### 2.1、下载Next主题

~~~bash
cd themes
git clone https://github.com/next-theme/hexo-theme-next.git next
cd next
git reset --hard v8.12.0
~~~



## 3、Next主题配置

### 3.1、启动主题

修改`_config.yml`配置文件

~~~yaml
theme: next
~~~



### 3.2、配置布局

编辑主题配置文件 `theme/next/_config.yml`

~~~yaml
# ---------------------------------------------------------------
# Scheme Settings
# ---------------------------------------------------------------

# Schemes
# scheme: Muse
#scheme: Mist
#scheme: Pisces
scheme: Gemini
~~~



### ~~3.3、配置语言~~

编辑主题配置文件 `theme/next/_config.yml`

~~~yaml
language: zh-Hans
~~~



### 3.4、菜单栏配置

编辑主题配置文件 `theme/next/_config.yml`

~~~bash
# ---------------------------------------------------------------
# Menu Settings
# ---------------------------------------------------------------

# Usage: `Key: /link/ || icon`
# Key is the name of menu item. If the translation for this item is available, the translated text will be loaded, otherwise the Key name will be used. Key is case-sensitive.
# Value before `||` delimiter is the target link, value after `||` delimiter is the name of Font Awesome icon.
# External url should start with http:// or https://
menu:
  home: / || fa fa-home
  #about: /about/ || fa fa-user
  tags: /tags/ || fa fa-tags
  #categories: /categories/ || fa fa-th
  archives: /archives/ || fa fa-archive
  #schedule: /schedule/ || fa fa-calendar
  #sitemap: /sitemap.xml || fa fa-sitemap
  #commonweal: /404/ || fa fa-heartbeat

# Enable / Disable menu icons / item badges.
menu_settings:
  icons: true
  badges: true
~~~



### 3.5、创建tags页面

~~~bash
hexo new page "tags"
~~~



### 3.6、设置侧边栏

编辑主题配置文件 `theme/next/_config.yml`

~~~bash
# ---------------------------------------------------------------
# Sidebar Settings
# See: https://theme-next.js.org/docs/theme-settings/sidebar
# ---------------------------------------------------------------

sidebar:
  # Sidebar Position.
  position: left
  #position: right

  # Manual define the sidebar width. If commented, will be default for:
  # Muse | Mist: 320
  # Pisces | Gemini: 240
  #width: 300

  # Sidebar Display (only for Muse | Mist), available values:
  #  - post    expand on posts automatically. Default.
  #  - always  expand for all pages automatically.
  #  - hide    expand only when click on the sidebar toggle icon.
  #  - remove  totally remove sidebar including sidebar toggle.
  display: post

  # Sidebar padding in pixels.
  padding: 18
  # Sidebar offset from top menubar in pixels (only for Pisces | Gemini).
  offset: 12
~~~



### 3.7、设置博客个人信息

编辑主题配置文件 `theme/next/_config.yml`

#### 3.7.1、设置头像

~~~bash
# Sidebar Avatar
avatar:
  # Replace the default image and set the url here.
  url: /images/avatar.jpg
  # If true, the avatar will be displayed in circle.
  rounded: true
  # If true, the avatar will be rotated with the cursor.
  rotated: true

~~~

#### 3.7.2、设置社交连接

~~~yaml
# Social Links
# Usage: `Key: permalink || icon`
# Key is the link label showing to end users.
# Value before `||` delimiter is the target permalink, value after `||` delimiter is the name of Font Awesome icon.
social:
  GitHub: https://github.com/Oort-ysf || fab fa-github
  E-Mail: mailto:ysf504703038@163.com || fa fa-envelope
  #Weibo: https://weibo.com/yourname || fab fa-weibo
  #Google: https://plus.google.com/yourname || fab fa-google
  #Twitter: https://twitter.com/yourname || fab fa-twitter
  #FB Page: https://www.facebook.com/yourname || fab fa-facebook
  #StackOverflow: https://stackoverflow.com/yourname || fab fa-stack-overflow
  #YouTube: https://youtube.com/yourname || fab fa-youtube
  #Instagram: https://instagram.com/yourname || fab fa-instagram
  #Skype: skype:yourname?call|chat || fab fa-skype
  
~~~



### 3.8、设置代码样式

编辑主题配置文件 `theme/next/_config.yml`

~~~yaml
codeblock:
  # Code Highlight theme
  # All available themes: https://theme-next.js.org/highlight/
  theme:
    light: monokai
    dark: monokai
  prism:
    light: prism
    dark: prism-dark
  # Add copy button on codeblock
  copy_button:
    enable: true
    # Available values: default | flat | mac
    style: mac

~~~



### 3.9、设置站点起始时间

编辑主题配置文件 `theme/next/_config.yml`

~~~yaml
since: 2017
~~~



### 3.10、设置背景动画

~~~yaml
# ---------------------------------------------------------------
# Animation Settings
# ---------------------------------------------------------------

# Use Animate.css to animate everything.
# For more information: https://animate.style
motion:
  enable: true
  async: false
  transition:
    # All available transition variants: https://theme-next.js.org/animate/
    post_block: fadeIn
    post_header: fadeInDown
    post_body: fadeInDown
    coll_header: fadeInLeft
    # Only for Pisces | Gemini.
    sidebar: fadeInUp

# Progress bar in the top during page loading.
# For more information: https://github.com/CodeByZach/pace
pace:
  enable: true
  # All available colors:
  # black | blue | green | orange | pink | purple | red | silver | white | yellow
  color: blue
  # All available themes:
  # big-counter | bounce | barber-shop | center-atom | center-circle | center-radar | center-simple
  # corner-indicator | fill-left | flat-top | flash | loading-bar | mac-osx | material | minimal
  theme: minimal

# Canvas ribbon
# For more information: https://github.com/hustcc/ribbon.js
canvas_ribbon:
  enable: true
  size: 300 # The width of the ribbon
  alpha: 0.6 # The transparency of the ribbon
  zIndex: -1 # The display level of the ribbon

~~~

