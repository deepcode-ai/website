---
created-on: 2023-12-05T16:13:07.942Z
f_long-description: >-
  ## Description


  Using event object APIs that are specific to `jQuery.Event`, such as `originalEvent`, is deprecated in Ember.js v3.3. This codemod ensures the access to the native event without triggering any deprecations via wrapping the `event` with the `normalizeEvent` function provided by `ember-jquery-legacy`.


  ## Example


  ### Before:


  ```typescript

  export default Component.extend({
  	click(event) {
  		let nativeEvent = event.originalEvent;
  	},
  });

  ```


  ### After:


  ```typescript

  import { normalizeEvent } from 'ember-jquery-legacy';


  export default Component.extend({
  	click(event) {
  		let nativeEvent = normalizeEvent(event);
  	},
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/ember-jquery-legacy
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=7ov34iPxeWaG6gKTD3mLR4ksgM0
f_codemod-studio-link: https://go.deepcode.io/86LYcy
f_cli-command: deepcode ember/5/ember-jquery-legacy
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.3.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Ember Jquery Legacy
updated-on: 2023-12-05T16:13:07.954Z
published-on: 2023-12-05T16:13:07.959Z
f_slug-name: ember-jquery-legacy
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:13:07.963Z
seo:
  title: Ember.js V5 - Ember Jquery Legacy | Deepcode Automations
  og:title: Ember.js V5 - Ember Jquery Legacy | Deepcode Automations
  twitter:title: Ember.js V5 - Ember Jquery Legacy | Deepcode Automations
  description: This codemod ensures access to the native event without triggering
    any deprecations via wrapping the `event` with the `normalizeEvent` function
    provided by `ember-jquery-legacy`.
  twitter:card: This codemod ensures access to the native event without triggering
    any deprecations via wrapping the `event` with the `normalizeEvent` function
    provided by `ember-jquery-legacy`.
  og:image: /assets/images/ember-jquery-legacy.jpg
---
This codemod ensures access to the native event without triggering any deprecations via wrapping the `event` with the `normalizeEvent` function provided by `ember-jquery-legacy`.