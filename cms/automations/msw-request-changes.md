---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description


  Following the original msw upgrade guide, the signature of the request handler have changed. Some of the parameters have changed their type, some widely used objects are available directly on the callback argument object for convenience. Following changes are applied by this codemod:


  * `req.url` is now obtained as `new URL(request.url)`, request being a new object available for destructure from the single callback argument.

  * `req.params` are now exposed in the same callback argument. 

  * `req.cookies` are now exposed in the same callback argument. 

  * `req.body` is now removed instead of being deprecated. New response object now has a `.json()` method that should be the preferred way.


  This codemod does not update the mentioned signatures of callback methods due to the fact that there are more changes in other codemods included in the `upgrade-recipe` that rely on the old signature. To apply the changes, you will have to run the recipe or run a `callback-signature` codemod that will do only that and replace all the references of old signature arguments.


  ## Example


  ### Before


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    const search = req.url.searchParams;
    const { cookies, body: reqBody, thing } = req;

    const { params } = req;

    const userCookies = req.cookies.user;
    const requestParams = req.params.thing;

    return res(ctx.json({ firstName: 'John' }));
  });

  ```


  ### After


  ```typescript

  import { setupWorker } from 'msw/browser'; import { http as caller, type HttpHandler } from 'msw';

  const handlers: HttpHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      const url = new URL(request.url);
      const search = url.searchParams;
      const { thing } = req;

      const userCookies = cookies.user;
      const requestParams = params.thing;

      return res(ctx.json({ firstName: 'John' }));
    }),
  ]

  ```


  ### Links for more info


  * [msw v1 to v2 migration guide -> request changes](https://mswjs.io/docs/migrations/1.x-to-2.x/#request-changes)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/request-changes
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=wSWbFD-5ULW68QMp4rgGW9G5SNQ
f_cli-command: deepcode msw/2/request-changes
f_framework: cms/framework/msw.md
f_applicability-criteria: MSW version >= 1.0.0
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-request-changes
title: Apply request changes
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-request-changes
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 15 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
This automation updates the request handler signature in the MSW library, changing how certain request properties are accessed and removing deprecated elements.