---
title: Quick Shopify Dev Tip #1
date: '2020-07-21'
tags: [Shopify, Dev]
draft: false
summary: Improve your Shopify theme's performance by using this new theme tag!
images:
  [
    'https://og.tracycodes.com/**Quick%20Shopify%20Dev%20Tip%20%231**.png?theme=dark&md=1&fontSize=100px',
  ]
---

![Quick Shopify Dev Tip #1](https://og.tracycodes.com/**Quick%20Shopify%20Dev%20Tip%20%231**.png?theme=dark&md=1&fontSize=100px)

In late 2019 Shopify deprecated the `{% include %}` tag in favor of `{% render %}` tag. This tag improves performance immensely as instead of automatically inheriting every variable assigned above the `{% include %}` tag, you have define each variable in your `{% render %}` tag. By doing so, you greatly reduce the time Shopify's liquid engine takes to render your snippets.

You can read more about how to use the new `{% render %}` tag here: [https://shopify.dev/docs/themes/liquid/reference/tags/theme-tags#render](https://shopify.dev/docs/themes/liquid/reference/tags/theme-tags#render)
