---
title: How To Setup Shopify Slate on Ubuntu
date: '2020-01-03'
tags: [Shopify, Web Dev]
draft: false
summary:
images:
  [https://og.tracycodes.com/**Shopify%20Slate%20on%20Ubuntu**.png?theme=dark&md=1&fontSize=100px]
---

![Shopify Slate on Ubuntu](https://og.tracycodes.com/**Shopify%20Slate%20on%20Ubuntu**.png?theme=dark&md=1&fontSize=100px)

So recently, I've started to make the move off MacOS as my daily work driver and was trying to work solely on my Windows 10 Laptop (Razer Blade). Well, it was all fine and dandy with my sweet WSL2 setup, until I encountered an issue. There's no official instructions on how to use Shopify Slate properly on Linux.

In this post, I'd like to document my steps taken to properly get a local SSL setup while still following Shopify Slate's instructions with their ssl-check shell function they provide you.

_Note: I've made a PR with documentation updates to the Shopify Slate repo!_

1. Follow all the [Shopify Slate instructions](https://shopify.github.io/slate/docs) up to the "Create a self-signed SSL certificate" step
2. Once at this step, you need to install mkcert by [following these instructions from the official mkcert repo](https://github.com/FiloSottile/mkcert#linux) and then [add this function](https://gist.github.com/tracy-codes/a9f292f840cc2ff331d7f53889eaccb3) to your shell/bash profile (.bash_profile, .zshrc, .bashrc, etc...)
3. Restart your terminal or run `source <location of your shell profile>`
4. Run ssl-check and then run mkcert -install
5. You will need to restart your currently open browsers for these changes to take effect
