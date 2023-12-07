---
created-on: 2023-12-05T16:08:37.906Z
f_long-description: >-
  ## Description


  This codemod removes all calls to `willTransition` or `didTransition` events on the Router via usage of `routeWillChange` event listener and `routeDidChange` event listener.


  ## Example


  ### Before:


  ```typescript

  import Router from '@ember/routing/router';

  import { inject as service } from '@ember/service';


  export default Router.extend({
  	currentUser: service('current-user'),

  	willTransition(transition) {
  		this._super(...arguments);
  		if (!this.currentUser.isLoggedIn) {
  			transition.abort();
  			this.transitionTo('login');
  		}
  	},

  	didTransition(privateInfos) {
  		this._super(...arguments);
  		ga.send('pageView', {
  			pageName: privateInfos.name,
  		});
  	},
  });

  ```


  ### After:


  ```typescript

  import Router from '@ember/routing/router';

  import { inject as service } from '@ember/service';


  export default Router.extend({
  	currentUser: service('current-user'),

  	init() {
  		this._super(...arguments);

  		this.on('routeWillChange', (transition) => {
  			if (!this.currentUser.isLoggedIn) {
  				transition.abort();
  				this.transitionTo('login');
  			}
  		});

  		this.on('routeDidChange', (transition) => {
  			ga.send('pageView', {
  				pageName: privateInfos.name,
  			});
  		});
  	},
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/deprecate-router-events
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=mwdY99AT40pd8fQUil33BeR7SEo
f_codemod-studio-link: https://go.deepcode.io/MYgG49
f_cli-command: deepcode ember/5/deprecate-router-events
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.6.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Deprecate Router Events
updated-on: 2023-12-05T16:08:37.915Z
published-on: 2023-12-05T16:08:37.922Z
f_slug-name: ember-deprecate-router-events
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:08:37.929Z
seo:
  title: Ember.js V5 - Deprecate Router Events | Deepcode Automations
  og:title: Ember.js V5 - Deprecate Router Events | Deepcode Automations
  twitter:title: Ember.js V5 - Deprecate Router Events | Deepcode Automations
  description: This automation removes all calls to `willTransition` or
    `didTransition` events on the Router via usage of `routeWillChange` event
    listener and `routeDidChange` event listener.
  twitter:card: This automation removes all calls to `willTransition` or
    `didTransition` events on the Router via usage of `routeWillChange` event
    listener and `routeDidChange` event listener.
  og:image: /assets/images/deprecate-router-events.jpg
---
This automation removes all calls to `willTransition` or `didTransition` events on the Router via usage of `routeWillChange` event listener and `routeDidChange` event listener.