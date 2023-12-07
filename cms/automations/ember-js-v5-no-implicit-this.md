---
created-on: 2023-12-05T17:04:42.668Z
f_long-description: >-
  ## Description


  This codemod removes all calls to `propertyWillChange` and replaces all calls to `propertyDidChange` with `notifyPropertyChange`.


  ## Example


  ### Before:


  ```typescript

  Ember.propertyWillChange(object, 'someProperty');

  doStuff(object);

  Ember.propertyDidChange(object, 'someProperty');


  object.propertyWillChange('someProperty');

  doStuff(object);

  object.propertyDidChange('someProperty');

  ```


  ### After:


  ```typescript

  doStuff(object);

  Ember.notifyPropertyChange(object, 'someProperty');


  doStuff(object);

  object.notifyPropertyChange('someProperty');

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/notify-property-change
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=TzYcFw0pbJTydA16tTFEvI3sM8M
f_codemod-studio-link: https://go.deepcode.io/XXlTDd
f_cli-command: deepcode ember/5/notify-property-change
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.1.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Notify Property Change
updated-on: 2023-12-05T17:04:42.678Z
published-on: 2023-12-05T17:04:42.685Z
f_slug-name: ember-notify-property-change
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T17:04:42.695Z
seo:
  title: Ember.js V5 - Notify Property Change | Deepcode Automations
  og:title: Ember.js V5 - Notify Property Change | Deepcode Automations
  twitter:title: Ember.js V5 - Notify Property Change | Deepcode Automations
  description: This automation removes all calls to `propertyWillChange` and
    replaces all calls to `propertyDidChange` with `notifyPropertyChange`.
  twitter:card: This automation removes all calls to `propertyWillChange` and
    replaces all calls to `propertyDidChange` with `notifyPropertyChange`.
  og:image: /assets/images/notify-property-change.jpg
---
This automation removes all calls to `propertyWillChange` and replaces all calls to `propertyDidChange` with `notifyPropertyChange`.