---
created-on: 2023-12-05T16:19:13.629Z
f_long-description: >-
  ## Description


  This codemod transforms `get()` to `getProperties()` to use traditional object dot notation. This standard was proposed by Ember.js team in https://github.com/emberjs/rfcs/blob/master/text/0281-es5-getters.md.


  ## Example


  ### Before:


  ```typescript

  let chancancode = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  chancancode.get('fullName');


  let model = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  model.get('fullName');


  let route = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  route.get('fullName');


  let controller = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  controller.get('fullName');

  controller.get('foo.bar');

  controller.get('foo-bar');

  ```


  ### After:


  ```typescript

  let chancancode = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  chancancode.get('fullName');


  let model = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  model.get('fullName');


  let route = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  route.fullName;


  let controller = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });


  controller.fullName;

  controller.get('foo.bar');

  controller['foo-bar'];

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/edit/main/codemods/ember/5/es5-getter-ember-codemod
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=gRfEFfyVMWOpWwejLmCFzbnPK8I
f_codemod-studio-link: https://go.deepcode.io/Ay4HST
f_cli-command: deepcode ember/5/es5-getter-ember-codemod
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.1.
f_verified-codemod: false
f_author: cms/authors/multiple-contributors-es5-getter-ember-codemod.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - ES5 Getter Ember Codemod
updated-on: 2023-12-05T16:19:13.634Z
published-on: 2023-12-05T16:19:13.641Z
f_slug-name: ember-es5-getter-ember-codemod
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:19:13.647Z
seo:
  title: Ember.js V5 - ES5 Getter Ember | Deepcode Automations
  og:title: Ember.js V5 - ES5 Getter Ember | Deepcode Automations
  twitter:title: Ember.js V5 - ES5 Getter Ember | Deepcode Automations
  description: This automation transforms `get()` to `getProperties()` to use
    traditional object dot notation.
  twitter:card: This automation transforms `get()` to `getProperties()` to use
    traditional object dot notation.
  og:image: /assets/images/es5-getter-ember.jpg
---
This automation transforms `get()` to `getProperties()` to use traditional object dot notation.