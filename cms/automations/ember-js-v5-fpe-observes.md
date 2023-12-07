---
created-on: 2023-12-05T16:32:38.087Z
f_long-description: >-
  ## Description


  This automation refactors observer definitions in Ember.js from using the `.observes` method to the modern `observer` function syntax.


  ## Example


  ### Before:


  ```typescript

  import EmberObject from '@ember/object';


  export default EmberObject.extend({
  	valueObserver: function () {
  		// Executes whenever the "value" property changes
  	}.observes('value'),
  });

  ```


  ### After:


  ```typescript

  import EmberObject from '@ember/object';


  export default EmberObject.extend({
  	valueObserver: observer('value', function () {
  		// Executes whenever the "value" property changes
  	}),
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/fpe-observes
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=r2pmqub8Ca8mvjAu-THl2YNei6k
f_codemod-studio-link: https://go.deepcode.io/U6OywE
f_cli-command: deepcode ember/5/fpe-observes
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.11.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Fpe Observes
updated-on: 2023-12-05T16:32:38.097Z
published-on: 2023-12-05T16:32:38.105Z
f_slug-name: ember-fpe-observes
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:32:38.112Z
seo:
  title: Ember.js V5 - Fpe Observes | Deepcode Automations
  og:title: Ember.js V5 - Fpe Observes | Deepcode Automations
  twitter:title: Ember.js V5 - Fpe Observes | Deepcode Automations
  description: This automation refactors observer definitions in Ember.js from
    using the `.observes` method to the modern `observer` function syntax.
  twitter:card: This automation refactors observer definitions in Ember.js from
    using the `.observes` method to the modern `observer` function syntax.
  og:image: /assets/images/fpe-observes.jpg
---
This automation refactors observer definitions in Ember.js from using the `.observes` method to the modern `observer` function syntax.