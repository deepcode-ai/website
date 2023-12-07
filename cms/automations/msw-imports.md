---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description

  Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will import correct objects from appropriate paths to start your msw migration path.

  -   `setupWorker` is now imported from `msw/browser`
  -   `rest` from `msw` is now named `http`
  -   `RestHandler` from `msw` is now named `HttpHandler`
  
  ## Example
  
  ### Before
  
  ```ts
  
  import { setupWorker, rest as caller, RestHandler } from 'msw';
  
  const handlers: RestHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]

  ```
  
  ### After
  
  ```ts

  import { setupWorker } from 'msw/browser';
  import { http as caller, HttpHandler } from 'msw';
  
  const handlers: HttpHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]

  ```
  ### Links for more info

  -   [msw v1 to v2 migration guide -> imports](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/imports
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=03s9tN6jERYILUlAfRX9cNotRpc
f_cli-command: deepcode msw/2/imports
f_applicability-criteria: "MSW version >= 1.0.0"
f_framework: cms/framework/msw.md
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-imports
title: Replace MSW Imports
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-imports
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 10 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
This codemod replaces MSW v1 with v2 imports.