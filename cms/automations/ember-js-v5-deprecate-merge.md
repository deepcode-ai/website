---
created-on: 2023-12-05T16:05:41.927Z
f_long-description: |-
  ## Description

  This codemod replaces all calls to `Ember.merge` with `Ember.assign`.

  ## Example

  ### Before:

  ```typescript
  import { merge } from '@ember/polyfills';

  var a = { first: 'Yehuda' };
  var b = { last: 'Katz' };
  merge(a, b);
  ```

  ### After:

  ```typescript
  import { assign } from '@ember/polyfills';

  var a = { first: 'Yehuda' };
  var b = { last: 'Katz' };
  assign(a, b);
  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/deprecate-merge
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=SwH9ekSK1NDUt3QxSb3Hl4VfdAU
f_codemod-studio-link: https://go.deepcode.io/SnbAVW
f_cli-command: deepcode ember/5/deprecate-merge
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.6.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Deprecate Merge
updated-on: 2023-12-05T16:05:41.933Z
published-on: 2023-12-05T16:05:41.939Z
f_slug-name: ember-deprecate-merge
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:05:41.946Z
seo:
  title: Ember.js V5 - Deprecate Merge | Deepcode Automations
  og:title: Ember.js V5 - Deprecate Merge | Deepcode Automations
  twitter:title: Ember.js V5 - Deprecate Merge | Deepcode Automations
  description: This automation replaces all calls to `Ember.merge` with `Ember.assign`.
  twitter:card: This automation replaces all calls to `Ember.merge` with `Ember.assign`.
  og:image: /assets/images/deprecate-merge.jpg
---
This automation replaces all calls to `Ember.merge` with `Ember.assign`.