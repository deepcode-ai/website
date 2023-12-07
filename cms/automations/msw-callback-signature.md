---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description

  Following the original msw upgrade guide, the signature of the request handler have changed. This codemod hard replaces the callback signature to the new one and cleans up unused variables.

  NOTE: This codemod should be applied after running all the other codemods present in the `upgrade-recipe` that are related to `req`, `res`, `ctx` objects. On its own, this codemod makes no sense to be run, and will most likely not do what you want.

  ### WARNING

  This codemod runs `.fixUnusedIdentifiers()` on a source file you are running it on. This would remove any   unused declarations in the file. This is due to atomicity of this mod, which blindly inserts the callback   structure into each msw handler callback and then cleans up the variables that are not used.

  ## Example

  ### Before

  ```ts

  import { http } from 'msw';

  http.get('/resource', (req, res, ctx) => {
    return HttpResponse.json({ id: 'abc-123' });
  });

  ```

  ### After

  ```ts

  import { http } from 'msw';

  http.get('/resource', () => {
    return HttpResponse.json({ id: 'abc-123' });
  });

  ```

  ### Before

  ```ts

  import { http } from 'msw';

  http.get('/resource', (req, res, ctx) => {
    const userCookie = cookies.user;
    const url = new URL(request.url);

    doSomething(url);
    userCookie.doSomething();

    return HttpResponse.json({ id: 'abc-123' });
  });

  ```

  ### After

  ```ts

  import { http } from 'msw';

  http.get('/resource', ({ request, cookies }) => {
    const userCookie = cookies.user;
    const url = new URL(request.url);

    doSomething(url);
    userCookie.doSomething();

    return HttpResponse.json({ id: 'abc-123' });
  });

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/msw/2/callback-signature
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=TRpuPrAm19dZGB0t5PHS13IeL_E
f_cli-command: deepcode msw/2/callback-signature
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: msw-callback-signature
title: Replace MSW handler signature
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_slug-name: msw-callback-signature
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: 10 minutes/occurrence
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
date: 2023-11-20T14:53:04.294Z
---
This codemod hard replaces the callback signature to the new one and cleans up unused variables.