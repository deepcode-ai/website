---
created-on: 2023-12-05T15:28:08.923Z
f_long-description: >-
  ## Description


  This codemod removes any usage of `new` with `A`, and calls `A` as a standard function.


  ## Example


  ### Before:


  ```typescript

  import { A } from '@ember/array'; let arr = new A(); 

  ```


  ### After:


  ```typescript

  import { A as emberA } from '@ember/array'; let arr = A(); 

  ```


  ### Links for more info


  * [Ember.js v5 - New Array Wrapper](https://deprecations.emberjs.com/v3.x/#toc_array-new-array-wrapper)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/array-wrapper
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=O6EOMpMfKAT8XBYI_9BmPbGjh2s
f_codemod-studio-link: https://go.deepcode.io/UDkfyb
f_cli-command: deepcode ember/5/array-wrapper
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.6.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - New Array Wrapper
updated-on: 2023-12-05T15:28:09.564Z
published-on: 2023-12-05T15:28:10.108Z
f_slug-name: ember-array-wrapper
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T15:28:22.444Z
seo:
  title: Ember.js V5 - New Array Wrapper | Deepcode Automations
  og:title: Ember.js V5 - New Array Wrapper | Deepcode Automations
  twitter:title: Ember.js V5 - New Array Wrapper | Deepcode Automations
  description: This automations removes any usage of `new` with `A`, and calls `A`
    as a standard function.
  twitter:card: This automations removes any usage of `new` with `A`, and calls
    `A` as a standard function.
  og:image: /assets/images/move-css-in-js-styles.jpg
---
This automation removes any usage of `new` with `A`, and calls `A` as a standard function.