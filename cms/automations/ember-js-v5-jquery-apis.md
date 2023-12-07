---
created-on: 2023-12-05T16:57:48.040Z
f_long-description: >-
  ## Description


  Using event object APIs that are specific to `jQuery.Event`, such as `originalEvent`, is deprecated in Ember.js v3.3. This codemod removes all calls to `originalEvent` in case of accessing properties that work with jQuery events as well as native events.


  ## Example


  ### Before:


  ```typescript

  // your event handler:

  export default Component.extend({
  	click(event) {
  		let x = event.originalEvent.clientX;
  	},
  });

  ```


  ### After:


  ```typescript

  // your event handler:

  export default Component.extend({
  	click(event) {
  		let x = event.clientX;
  	},
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/jquery-event
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=8MIYv6K3Szow4WVYdgq1xyxfCT8
f_codemod-studio-link: https://go.deepcode.io/k6EGj4
f_cli-command: deepcode ember/5/jquery-event
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.3.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Jquery Event
updated-on: 2023-12-05T16:57:48.051Z
published-on: 2023-12-05T16:57:48.059Z
f_slug-name: ember-jquery-event
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:57:48.065Z
seo:
  title: Ember.js V5 - Jquery Event | Deepcode Automations
  og:title: Ember.js V5 - Jquery Event | Deepcode Automations
  twitter:title: Ember.js V5 - Jquery Event | Deepcode Automations
  description: This automation removes all calls to `originalEvent` in case of
    accessing properties that work with jQuery events as well as native events.
  twitter:card: This automation removes all calls to `originalEvent` in case of
    accessing properties that work with jQuery events as well as native events.
  og:image: /assets/images/jquery-event.jpg
---
This automation removes all calls to `originalEvent` in case of accessing properties that work with jQuery events as well as native events.