---
title: 'Quick Shopify Dev Tip #3'
date: '2020-07-24'
tags: [Shopify, Dev]
draft: false
summary: Make sure you're renaming your shopify sections with Shpify Schema or else you'll be left with a mess.
images:
  [
    'https://og.tracycodes.com/**Quick%20Shopify%20Dev%20Tip%20%233**.png?theme=dark&md=1&fontSize=100px',
    '/static/images/shopify-section-hell.png',
  ]
---

![Quick Shopify Dev Tip #3](https://og.tracycodes.com/**Quick%20Shopify%20Dev%20Tip%20%233**.png?theme=dark&md=1&fontSize=100px)

Any sections you create will show u in the customizer for the homepage as a section that can be added dynamically. To make sure you avoid confusion for your customers/clients, make sure you use Shopify Schema's "name" field for your sections. It's common practice to duplicate sections for new page templates so you can have separate content. You don't want to end up with this as options in your home page's Customizer:

![Shopify Section Hell](/static/images/shopify-section-hell.png)

You can read more about Shopify's Theme Section Schema here: [https://shopify.dev/tutorials/develop-theme-use-sections#name](https://shopify.dev/tutorials/develop-theme-use-sections#name)
