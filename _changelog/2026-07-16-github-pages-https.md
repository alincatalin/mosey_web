---
title: The harmless redirect that broke HTTPS
date: 2026-07-16
categories: [fix, learn]
tags: [github-pages, dns, https]
---
I set up the site on GitHub Pages, but HTTPS would not provision. Namecheap still had a URL redirect from `@` to `www.usemosey.app`. It looked harmless, but it made the root domain resolve through an extra IP.

Removing the redirect, confirming that only GitHub's four A records remained, and re-adding the custom domain in GitHub Pages fixed it.

Future reminder: URL redirects can silently interfere with GitHub Pages HTTPS, even when the visible DNS records look correct.
