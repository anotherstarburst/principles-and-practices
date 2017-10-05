---
layout: page
title: Web Development practices
---

## Vendor prefixes

Do not use vendor prefixes. Stick to the standard prefix and let the functionality take effect when it is ready.

Chrome in particular changes functionality between releases in vendor-only implementations.

## CSS

CSS should be written in CSS.

Where we collaborate with external designers they commonly want to use SASS, which is fine but we should build a deployment versions and use the POP CSS project to distribute it.