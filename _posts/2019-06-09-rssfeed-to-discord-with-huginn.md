---
layout: post
title: 'RSSFeed to discord with Huginn'
date: 2019-06-09
categories: [Tutorial]
comments: true
thumbnail: assets/img/contoh_thumbnail.png
---

# rssfeed to discord with Huginn
Tutorial How to make autopost bot discord from rss feed website.

# Event Flow

[![flowevent.jpg](https://s3.gifyu.com/images/flowevent.jpg)](https://gifyu.com/image/EcJS)

# Setup Discord
- Server settings > webhooks > create webhooks
- save your webhooks url

# Setup Huginn
- Deploy [Huginn](https://github.com/rokhimin/huginn-test) to your server ( I recommended Heroku )

## Rss Agent
- schedule : 1m (5m,10m whatever)
- receiver : formatter agent
- set your url rss feed

![example](https://s3.gifyu.com/images/huginn0.jpg)

## Formatter Agent
- (Optional) You can use a trigger agent
- source : rss agent
- receiver : post agent
- example

![example](https://s3.gifyu.com/images/huginn1.jpg)

- use [liquid filter](https://help.shopify.com/en/themes/liquid/filters/string-filters) to filtering your rss

## Post Agent
- schedule : never
- source : formatter agent
- example

![example](https://s3.gifyu.com/images/huginn2.jpg)

- dry run to test

[![rssdiscord-whd-28922.jpg](https://s3.gifyu.com/images/rssdiscord-whd-28922.jpg)](https://gifyu.com/image/EcJq)





