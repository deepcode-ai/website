---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description


  To send a response from MSW handler, one would previously use something like `res(ctx.text("Hello world"))`. In msw v2, this is achieved by returning a native WebAPI Response object. msw v2 conveniently exposes a `HttpResponse` function that has useful methods for creating just that object with a desired body. This codemod replaces the old `res` calls with the new `HttpResponse` function calls and a bunch of ctx utilities that usually go with it. See examples below.


  This codemod does not remove unused properties on the callback signature due to the fact that there are more changes in other codemods included in the `upgrade-recipe` that rely on it. To apply these changes, you will have to run the recipe or run a `callback-signature` codemod that will do only that and replace all the references of old signature arguments.


  ## Example


  ### Before


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return res(
      ctx.json({ id: "abc-123" }),
      ctx.cookie("roses", "red"),
      ctx.cookie("violets", "blue"),
      ctx.set("X-Custom", "value")
    );
  });

  ```


  ### After


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return HttpResponse.json({ id: 'abc-123' }, {
      headers: {
        'X-Custom': 'value',
        'Set-Cookie': 'roses=red;violets=blue;',
      },
    });
  });

  ```


  ### Before


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return res(
      ctx.text("Hello world!"),
      ctx.delay(500),
      ctx.status(401)
    );
  });

  ```


  ### After


  ```typescript

  import { rest, delay } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    await delay(500);

    return HttpResponse.text("Hello world", {
      status: 401,
    });
  });

  ```


  ### Before


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return res(
      ctx.body('Hello world!'),
      ctx.set('Content-Type', 'text/plain'),
    );
  });

  ```


  ### After


  ```typescript

  import { rest, delay } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return HttpResponse.text("Hello world");
  });

  ```


  ### Before


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return res(ctx.text('Hello world!'));
  });

  ```


  ### After


  ```typescript

  import { rest } from 'msw';

  rest.get('/user', (req, res, ctx) => {
    return HttpResponse.text("Hello world");
  });

  ```


  ### Before


  ```typescript

  graphql.query('GetUser', (req, res, ctx) => {
    return res(
      ctx.data({
        user: { firstName: 'John' },
      }),
      ctx.errors([
        { message: `Failed to login:  user "${username}" does not exist` },
      ]),
      ctx.extensions({
        requestId: 'abc-123',
      })
    )
  })

  ```


  ### After


  ````typescript

  graphql.query('GetUser', (req, res, ctx) => {
    return HttpResponse.json(
      data: {
        user: { firstName: 'John' },
      },
      errors: [
        { message: `Failed to login:  user "${username}" does not exist` },
      ],
      extensions: {
        requestId: 'abc-123',
      },
    )
  })

  ``` ### Links for more info

  -   [msw v1 to v2 migration guide -> response usages](https://mswjs.io/docs/migrations/1.x-to-2.x/#request-changes)

  ````


  ### Links for more info


  * [msw v1 to v2 migration guide -> request changes](https://mswjs.io/docs/migrations/1.x-to-2.x/#request-changes)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/response-usages
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=xAFwkrXvZOF0QbeiBWcvwm8WpDI
f_cli-command: deepcode msw/2/response-usages
f_framework: cms/framework/msw.md
f_applicability-criteria: MSW version >= 1.0.0
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-response-usages
title: Update Response Usages
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-response-usages
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 10 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
This automation updates MSW handlers to use the new HttpResponse function for responses, replacing old `res` calls with this new method in msw v2.