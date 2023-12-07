---
created-on: 2023-12-05T16:01:45.947Z
f_long-description: >-
  ## Description


  This codemod removes all calls to `volatile()` and ensures that native getters are directly used.


  ## Example


  ### Before:


  ```typescript

  const Person = EmberObject.extend({
  	fullName: computed(function () {
  		return `${this.firstName} ${this.lastName}`;
  	}).volatile(),
  });

  ```


  ### After:


  ```typescript

  const Person = EmberObject.extend({
  	get fullName() {
  		return `${this.firstName} ${this.lastName}`;
  	},
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/cp-volatile
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=t0qpljVDAowX4w-aSSghMAMIa38
f_codemod-studio-link: https://go.deepcode.io/XtmaVa
f_cli-command: deepcode ember/5/cp-volatile
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.9.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Cp Volatile
updated-on: 2023-12-05T16:01:45.955Z
published-on: 2023-12-05T16:01:45.960Z
f_slug-name: ember-cp-volatile
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:01:45.964Z
seo:
  title: Ember.js V5 - Cp Volatile | Deepcode Automations
  og:title: Ember.js V5 - Cp Property Volatile | Deepcode Automations
  twitter:title: Ember.js V5 - Cp Volatile | Deepcode Automations
  description: This automation removes all calls to `volatile()` and ensures that
    native getters are directly used.
  twitter:card: This automation removes all calls to `volatile()` and ensures that
    native getters are directly used.
  og:image: /assets/images/cp-volatile.jpg
---
This automation removes all calls to `volatile()` and ensures that native getters are directly used.