---
created-on: 2023-11-01T18:16:50.459Z
f_long-description: >-
  ## Description


  This codemod replaces all occurrences of `this.currentRouteName` with `this.router.currentRouteName`

  and `this.currentPath` with `this.router.currentPath`.


  ## Example


  ### Before:


  ```typescript

  import Controller from '@ember/controller';

  import fetch from 'fetch';


  export default Controller.extend({
  	store: service('store'),

  	actions: {
  		sendPayload() {
  			fetch('/endpoint', {
  				method: 'POST',
  				body: JSON.stringify({
  					route: this.currentRouteName,
  				}),
  			});
  		},
  	},
  });

  ```


  ### After:


  ```typescript

  import Controller from '@ember/controller';

  import fetch from 'fetch';


  export default Controller.extend({
  	router: service('router'),
  	store: service('store'),

  	actions: {
  		sendPayload() {
  			fetch('/endpoint', {
  				method: 'POST',
  				body: JSON.stringify({
  					route: this.router.currentRouteName,
  				}),
  			});
  		},
  	},
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/app-controller-router-props
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=2ilOsMOt-d18XxYxfiO3RhiKtOI
f_codemod-studio-link: https://go.deepcode.io/xmT5B0
f_cli-command: deepcode ember/5/app-controller-router-props
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.10.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-app-controller-router-props
title: Ember.js V5 - App Controller Router Props
updated-on: 2023-11-17T15:17:45.723Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: app-controller-router-props
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T15:30:13.935Z
seo:
  title: Ember.js V5 - App Controller Router Props | Deepcode Automations
  og:title: Ember.js V5 - App Controller Router Props | Deepcode Automations
  twitter:title: Ember.js V5 - App Controller Router Props | Deepcode Automations
  description: This codemod replaces all occurrences of `this.currentRouteName`
    with `this.router.currentRouteName` and `this.currentPath` with
    `this.router.currentPath`.
  twitter:card: This codemod replaces all occurrences of `this.currentRouteName`
    with `this.router.currentRouteName` and `this.currentPath` with
    `this.router.currentPath`.
  og:image: /assets/images/app-controller-router-props.jpg
---
This codemod replaces all occurrences of `this.currentRouteName` with `this.router.currentRouteName` and `this.currentPath` with `this.router.currentPath`.