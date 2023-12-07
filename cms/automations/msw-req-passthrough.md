---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description
  
  A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.
  
  ## Example
  
  ### Before
  
  ```ts

  rest.get('/resource', (req, res, ctx) => {
    return req.passthrough()
  })

  ```
  
  ### After
  
  ```ts

  import { passthrough } from 'msw'
  
  rest.get('/resource', (req, res, ctx) => {
    return passthrough()
  })

  ```
  
  ### Links for more info

  -   [msw v1 to v2 migration guide -> req passthrough](https://mswjs.io/docs/migrations/1.x-to-2.x/#reqpassthrough)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/req-passthrough
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=SHuKC96klArO3YKWCrmydNvoQl8
f_cli-command: deepcode msw/2/req-passthrough
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-req-passthrough
title: Replace printHandlers() calls
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-req-passthrough
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.