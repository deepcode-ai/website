---
created-on: 2023-12-05T17:23:11.284Z
f_long-description: >-
  ## Description


  `new EmberObject()` is deprecated in Ember.js v3.9 in favor of constructing instances of `EmberObject` and its subclasses. This codemod replaces all calls to `new EmberObject()` with `EmberObject.create()` and adds a `constructor` function to classes that extend from `EmberObject` so that the classes no longer extend from `EmberObject`.


  ## Example


  ### Before:


  ```typescript

  let obj1 = new EmberObject();

  let obj2 = new EmberObject({ prop: 'value' });


  const Foo = EmberObject.extend();

  let foo = new Foo({ bar: 123 });

  ```


  ### After:


  ```typescript

  let obj1 = EmberObject.create();

  let obj2 = EmberObject.create({ prop: 'value' });


  const Foo = EmberObject.extend();

  let foo = new Foo({ bar: 123 });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/object-new-constructor
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=DByr5sk2809c2rfO8_TvT-RB0Pw
f_codemod-studio-link: https://go.deepcode.io/RTN3yv
f_cli-command: deepcode ember/5/object-new-constructor
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.6.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Object New Constructor
updated-on: 2023-12-05T17:23:11.291Z
published-on: 2023-12-05T17:23:11.298Z
f_slug-name: ember-object-new-constructor
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T17:23:11.303Z
seo:
  title: Ember.js V5 - Object New Constructor | Deepcode Automations
  og:title: Ember.js V5 - Object New Constructor | Deepcode Automations
  twitter:title: Ember.js V5 - Object New Constructor | Deepcode Automations
  description: This codemod replaces all calls to `new EmberObject()` with
    `EmberObject.create()` and adds a `constructor` function to classes that
    extend from `EmberObject` so that the classes no longer extend from
    `EmberObject`.
  twitter:card: This codemod replaces all calls to `new EmberObject()` with
    `EmberObject.create()` and adds a `constructor` function to classes that
    extend from `EmberObject` so that the classes no longer extend from
    `EmberObject`.
  og:image: /assets/images/object-new-constructor.jpg
---
This codemod replaces all calls to `new EmberObject()` with `EmberObject.create()` and adds a `constructor` function to classes that extend from `EmberObject` so that the classes no longer extend from `EmberObject`.