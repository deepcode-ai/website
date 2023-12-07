---
created-on: 2023-12-05T15:58:45.749Z
f_long-description: >-
  ## Description


  `.property()` is a modifier that adds additional property dependencies to an existing computed property. This codemod moves the dependencies to the main computed property definition.


  ## Example


  ### Before:


  ```typescript

  const Person = EmberObject.extend({
  	fullName: computed(function () {
  		return `${this.firstName} ${this.lastName}`;
  	}).property('firstName', 'lastName'),
  });

  ```


  ### After:


  ```typescript

  const Person = EmberObject.extend({
  	fullName: computed('firstName', 'lastName', function () {
  		return `${this.firstName} ${this.lastName}`;
  	}),
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/cp-property
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=UEjLA-WkII1TJWdF-uBUDh_EGtk
f_codemod-studio-link: https://go.deepcode.io/ZTJPNB
f_cli-command: deepcode ember/5/cp-property
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.9.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Cp Property
updated-on: 2023-12-05T15:58:45.761Z
published-on: 2023-12-05T15:58:45.766Z
f_slug-name: ember-cp-property
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T15:58:45.777Z
seo:
  title: Ember.js V5 - Cp Property | Deepcode Automations
  og:title: Ember.js V5 - Cp Property Map | Deepcode Automations
  twitter:title: Ember.js V5 - Cp Property | Deepcode Automations
  description: This automation modifies the `.property()` to move additional
    property dependencies directly into the main definition of an existing
    computed property.
  twitter:card: This automation modifies the `.property()` to move additional
    property dependencies directly into the main definition of an existing
    computed property.
  og:image: /assets/images/cp-property.jpg
---
This automation modifies the `.property()` to move additional property dependencies directly into the main definition of an existing computed property.