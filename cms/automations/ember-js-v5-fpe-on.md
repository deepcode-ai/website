---
created-on: 2023-12-05T16:43:19.821Z
f_long-description: >-
  ## Example


  This codemod updates event handling in Ember.js by transitioning from the `.on` method to using the `on` function for event listeners.


  ### Before:


  ```typescript

  import EmberObject from '@ember/object';

  import { sendEvent } from '@ember/object/events';


  let Job = EmberObject.extend({
  	logCompleted: function () {
  		console.log('Job completed!');
  	}.on('completed'),
  });


  let job = Job.create();


  sendEvent(job, 'completed'); // Logs 'Job completed!'

  ```


  ### After:


  ```typescript

  import { on } from '@ember/object/evented';

  import EmberObject from '@ember/object';

  import { sendEvent } from '@ember/object/events';


  let Job = EmberObject.extend({
  	logCompleted: on('completed', function () {
  		console.log('Job completed!');
  	}),
  });


  let job = Job.create();


  sendEvent(job, 'completed'); // Logs 'Job completed!'

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/ember/5/fpe-on
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=cWArI_-rju-0ezn7eeit71rEfwI
f_codemod-studio-link: https://go.deepcode.io/vw0bbk
f_cli-command: deepcode ember/5/fpe-on
f_framework: cms/framework/ember-js.md
f_applicability-criteria: Ember.js version higher or equal to 3.11.
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-array-wrapper
title: Ember.js V5 - Fpe On
updated-on: 2023-12-05T16:43:19.831Z
published-on: 2023-12-05T16:43:19.838Z
f_slug-name: ember-fpe-on
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/ember-js-v5.md
tags: automations
date: 2023-12-05T16:43:19.844Z
seo:
  title: Ember.js V5 - Fpe On | Deepcode Automations
  og:title: Ember.js V5 - Fpe On | Deepcode Automations
  twitter:title: Ember.js V5 - Fpe On | Deepcode Automations
  description: This automation updates event handling in Ember.js by transitioning
    from the `.on` method to using the `on` function for event listeners.
  twitter:card: This automation updates event handling in Ember.js by
    transitioning from the `.on` method to using the `on` function for event
    listeners.
  og:image: /assets/images/fpe-on.jpg
---
This automation updates event handling in Ember.js by transitioning from the `.on` method to using the `on` function for event listeners.