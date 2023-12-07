---
created-on: 2023-12-05T15:43:26.874Z
f_long-description: >-
  ## Description


  This codemod transforms from the older `moduleFor*` syntax of `ember-qunit@2` to the newer `setup*Test` syntax.


  ## Example


  ### Before:


  ```typescript

  import { moduleFor, test } from 'ember-qunit';


  moduleFor('service:flash', 'Unit | Service | Flash', {
  	unit: true,
  });


  test('should allow messages to be queued', function (assert) {
  	let subject = this.subject();
  });

  ```


  ### After:


  ```typescript

  import { module, test } from 'qunit';

  import { setupTest } from 'ember-qunit';


  module('Unit | Service | Flash', function (hooks) {
  	setupTest(hooks);

  	test('should allow messages to be queued', function (assert) {
  		let subject = this.owner.lookup('service:flash');
  	});
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/convert-module-for-to-setup-test
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=VTupulWTlhXH3W_vzfSGItBnJM4
f_codemod-studio-link: https://go.deepcode.io/9k2w4p
f_cli-command: deepcode ember/5/convert-module-for-to-setup-test
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 2.4.
f_verified-codemod: false
f_author: cms/authors/robert-jackson.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Convert moduleFor to setupTest
updated-on: 2023-12-05T15:43:26.885Z
published-on: 2023-12-05T15:43:26.896Z
f_slug-name: ember-convert-module-for-to-setup-test
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T15:43:26.903Z
seo:
  title: Ember.js V5 - Convert moduleFor to setupTest | Deepcode Automations
  og:title: Ember.js V5 - Convert moduleFor to setupTest | Deepcode Automations
  twitter:title: Ember.js V5 - Convert moduleFor to setupTest | Deepcode Automations
  description: This automation transforms from the older `moduleFor*` syntax of
    `ember-qunit@2` to the newer `setup*Test` syntax.
  twitter:card: This automation transforms from the older `moduleFor*` syntax of
    `ember-qunit@2` to the newer `setup*Test` syntax.
  og:image: /assets/images/convert-modulefor-to-setuptest.jpg
---
This automation transforms from the older `moduleFor*` syntax of `ember-qunit@2` to the newer `setup*Test` syntax.