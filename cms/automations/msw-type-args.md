---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description

  There is a change to generic type interface of rest.method() calls. This codemod puts the generic arguments in the correct order to keep type safety.

  ### WARNING

  This codemod runs `.fixUnusedIdentifiers()` on a source file you are running it on. This would remove any unused declarations in the file. This is due to atomicity of this mod, which blindly inserts the callback structure into each msw handler callback and then cleans up the variables that are not used.

  ## Example

  ### Before

  ```ts

  http.get<ReqBodyType, PathParamsType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });

  ```

  ### After

  ```ts

  http.get<PathParamsType, ReqBodyType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });

  ```

  ### Before

  ```ts

  http.get<ReqBodyType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });

  ```

  ### After

  ```ts

  http.get<any, ReqBodyType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });

  ```

  ### Before

  ```ts

  const handlers: RestHandler<DefaultBodyType>[] = [
    http.get('/resource', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ];

  ```

  ### After

  ```ts

  const handlers: HttpHandler[] = [
    http.get<any, DefaultBodyType>('/resource', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ];

  ```

  ### Before

  ```ts

  export function mockFactory(
    url: string,
    resolver: ResponseResolver<
      MockedRequest<{ id: string }>,
      RestContext,
      Awaited<ImportedPromiseBodyType>
    >,
  ) {
    return http.get(url, resolver);
  };

  ```

  ### After

  ```ts

  export function mockFactory(
    url: string,
    resolver: ResponseResolver<
      HttpRequestResolverExtras<PathParams>,
      { id: string },
      Awaited<ImportedPromiseBodyType>
    >,
  ) {
    return http.get(url, resolver);
  };

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/type-args
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=6rdxdJ7YioUlKoq-z-4iFPeN3Rs
f_cli-command: deepcode msw/2/type-args
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-type-args
title: Move Generic Arguments and Body Type Casts
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-type-args
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 15 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
This automation puts the generic arguments in the correct order to keep type safety.