---
created-on: 2023-11-30T17:34:17.334Z
f_long-description: >-
  ## Description


  Since Next.js 13.4, you can mark the files that contain only client-side code with the `use client` directive at the top.


  The codemod will look for identifiers and string literals common for files that contain client-side code, such as React hooks or event handlers. On the other hand, it will not upsert any directive should it spot elements indicating server-side code.


  The codemod will not remove the existing `use client` directive even if it would suggest otherwise due to the code in question.


  ## Example


  ### Before


  ```typescript

  import { useState } from 'react';


  export default function Page() {
  	const [x, setX] = useState('');

  	return x;
  }

  ```


  ### After


  ```typescript

  'use client';

  import { useState } from 'react';


  export default function Page() {
  	const [x, setX] = useState('');

  	return x;
  }

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/upsert-use-client-directive
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=f_fR6Z-Q5qlxnPnHK5-tpeNckVw
f_cli-command: deepcode next/13/upsert-use-client-directive
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 13.4.
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Upsert Use Client Directive
updated-on: 2023-11-30T17:34:17.353Z
published-on: 2023-11-30T17:34:17.359Z
f_slug-name: upsert-use-client-directive
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T17:34:17.366Z
seo:
  title: Next.js Upsert Use Client Directive | Deepcode Automations
  og:title: Next.js Upsert Use Client Directive | Deepcode Automations
  twitter:title: Next.js Upsert Use Client Directive | Deepcode Automations
  description: The automation will look for identifiers and string literals common
    for files that contain client-side code, such as React hooks or event
    handlers.
  twitter:card: The automation will look for identifiers and string literals
    common for files that contain client-side code, such as React hooks or event
    handlers.
  og:image: /assets/images/upsert-use-client-directive.jpg
---
The automation will look for identifiers and string literals common for files that contain client-side code, such as React hooks or event handlers.