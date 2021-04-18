---
title: Quick Shopify Dev Tip #2
date: '2020-07-22'
tags: [Shopify, Dev]
draft: false
summary: Add and improve your Shopify App's code automatically from a theme! Nobody likes an angry customer after they've tried to uninstall your app.
images:
  [
    'https://og.tracycodes.com/**Quick%20Shopify%20Dev%20Tip%20%232**.png?theme=dark&md=1&fontSize=100px',
  ]
---

![Quick Shopify Dev Tip #2](https://og.tracycodes.com/**Quick%20Shopify%20Dev%20Tip%20%232**.png?theme=dark&md=1&fontSize=100px)

If you're building a Shopify App that injects code into the storefront, make sure it can also remove that code automatically on install. Nothing is worse than a customer trying to remove your app and having to dig into their theme's code and then angrily leaving you a review afterwards.

To make this a smooth process on your end, what you can do is create separate snippets with the code you want on the store, then update theme.liquid or any other template/section with `{% render %}` tags (see [this post](/blog/quick-shopify-dev-tip-1) to learn about the new render tag) to have your code be included in the theme itself.

You can read more about Shopify's Theme API endpoints here: [https://shopify.dev/docs/admin-api/rest/reference/online-store/theme](https://shopify.dev/docs/admin-api/rest/reference/online-store/theme)

You can read more about how to add/remove/manage files from specific themes through the Theme Asset API endpoint here: [https://shopify.dev/docs/admin-api/rest/reference/online-store/asset](https://shopify.dev/docs/admin-api/rest/reference/online-store/asset)
