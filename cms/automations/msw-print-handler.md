---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description
  
  A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.
  
  ## Example
  
  ### Before
  
  ```ts

  worker.printHandlers()

  ```
  
  ### After
  
  ```ts

  worker.listHandlers().forEach((handler) => {
    console.log(handler.info.header)
  })

  ```
  
  ### Links for more info

  -   [msw v1 to v2 migration guide -> print handlers](https://mswjs.io/docs/migrations/1.x-to-2.x/#printhandlers)
  
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/print-handler
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=HvNEhmVfoqpwAcVZt7U9xaYBS2o
f_cli-command: deepcode msw/2/print-handler
f_framework: cms/framework/msw.md
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-print-handler
title: Replace printHandlers() calls
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-print-handler
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_applicability-criteria: "MSW version >= 1.0.0"
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.