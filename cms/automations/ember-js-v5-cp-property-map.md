---
created-on: 2023-12-05T15:51:27.073Z
f_long-description: >-
  ## Description


  `.property()` is a modifier that adds additional property dependencies to an existing computed property. For `filter`, `map`, and `sort` computed property macros, this codemod ensures they receive an array of additional dependent keys as a second parameter.


  ## Example


  ### Before:


  ```typescript

  const Person = EmberObject.extend({
  	friendNames: map('friends', function (friend) {
  		return friend[this.get('nameKey')];
  	}).property('nameKey'),
  });

  ```


  ### After:


  ```typescript

  const Person = EmberObject.extend({
  	friendNames: map('friends', ['nameKey'], function (friend) {
  		return friend[this.get('nameKey')];
  	}),
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/cp-property-map
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=T2qg3WOT4qOdTHg0LnDcfh16j30
f_codemod-studio-link: https://go.deepcode.io/7Uw5Jb
f_cli-command: deepcode ember/5/cp-property-map
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 2.4.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Cp Property Map
updated-on: 2023-12-05T15:51:27.082Z
published-on: 2023-12-05T15:51:27.088Z
f_slug-name: ember-cp-property-map
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T15:51:27.095Z
seo:
  title: Ember.js V5 - Cp Property Map | Deepcode Automations
  og:title: Ember.js V5 - Cp Property Map | Deepcode Automations
  twitter:title: Ember.js V5 - Cp Property Map | Deepcode Automations
  description: This automation adds extra property dependencies to computed
    properties like `filter`, `map`, and `sort`, automating the inclusion of an
    array of dependent keys as a second parameter.
  twitter:card: This automation adds extra property dependencies to computed
    properties like `filter`, `map`, and `sort`, automating the inclusion of an
    array of dependent keys as a second parameter.
  og:image: /assets/images/cp-property-map.jpg
---
This automation adds extra property dependencies to computed properties like `filter`, `map`, and `sort`, automating the inclusion of an array of dependent keys as a second parameter.