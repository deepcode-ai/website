---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description
  
  In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.
  
  ## Example
  
  ### Before
  
  ```ts

  server.events.on("request:start", (req, reqId) => {
    doStuff(req, reqId);
  });

  ```
  
  ### After
  
  ```ts

  server.events.on("request:start", ({ request, requestId }) => {
    doStuff(request, requestId);
  });

  ```

  ### Links for more info

  -   [msw v1 to v2 migration guide -> lifecycle events](https://mswjs.io/docs/migrations/1.x-to-2.x/#life-cycle-events)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/lifecycle-events-signature
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=DIAvSd9O-rhmXNGuTbHlOROvz6U
f_cli-command: deepcode msw/2/lifecycle-events-signature
f_applicability-criteria: "MSW version >= 1.0.0"
f_framework: cms/framework/msw.md
f_verified-codemod: false
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-lifecycle-events-signature
title: Replace lifecycle events callback signature [BETA]
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-lifecycle-events-signature
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.