---
created-on: 2023-12-05T16:25:52.222Z
f_long-description: |-
  ## Description

  ## Example

  ### Before:

  ```typescript
  import EmberObject from '@ember/object';

  let Person = EmberObject.extend({
  	init() {
  		this._super(...arguments);

  		this.firstName = 'Betty';
  		this.lastName = 'Jones';
  	},

  	fullName: function () {
  		return `${this.firstName} ${this.lastName}`;
  	}.property('firstName', 'lastName'),
  });

  let client = Person.create();

  client.get('fullName'); // 'Betty Jones'

  client.set('lastName', 'Fuller');
  client.get('fullName'); // 'Betty Fuller'
  ```

  ### After:

  ```typescript
  import { computed } from '@ember/object';
  import EmberObject from '@ember/object';

  let Person = EmberObject.extend({
  	init() {
  		this._super(...arguments);

  		this.firstName = 'Betty';
  		this.lastName = 'Jones';
  	},

  	fullName: computed('firstName', 'lastName', function () {
  		return `${this.firstName} ${this.lastName}`;
  	}),
  });

  let client = Person.create();

  client.get('fullName'); // 'Betty Jones'

  client.set('lastName', 'Fuller');
  client.get('fullName'); // 'Betty Fuller'
  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/ember/5/fpe-computed
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=jisEa59u6ByQ-XI9pMkBa_GsvCw
f_codemod-studio-link: https://go.deepcode.io/du04dP
f_cli-command: deepcode ember/5/fpe-computed
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.11.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Fpe Computed
updated-on: 2023-12-05T16:25:52.232Z
published-on: 2023-12-05T16:25:52.240Z
f_slug-name: ember-fpe-computed
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:25:52.246Z
seo:
  title: Ember.js V5 - Fpe Computed | Deepcode Automations
  og:title: Ember.js V5 - Fpe Computed | Deepcode Automations
  twitter:title: Ember.js V5 - Fpe Computed | Deepcode Automations
  description: The "Fpe Computed" codemod for Ember.js V5 refactors computed
    property definitions from the older `.property` method to the modern
    `computed` function syntax.
  twitter:card: The "Fpe Computed" codemod for Ember.js V5 refactors computed
    property definitions from the older `.property` method to the modern
    `computed` function syntax.
  og:image: /assets/images/fpe-computed.jpg
---
The "Fpe Computed" codemod for Ember.js V5 refactors computed property definitions from the older `.property` method to the modern `computed` function syntax.