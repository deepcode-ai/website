---
created-on: 2023-11-30T17:10:02.973Z
f_long-description: >-
  ## Description


  Since Next.js 13.4, you can use the following hooks from the `next/navigation` module:


  * `useRouter`,

  * `useSearchParams`,

  * `usePathname`,

  * `useParams`.


  These hooks replace the functionality available in the `useRouter` hook in the `next/hook` module, however, the behavior is distinct.


  This codemod allows you to migrate the `useRouter` hook to the new `useRouter` hook imported from `next/navigation`. This includes all usages of the `useRouter` hook which may be replaced with `useSearchParams` and `usePathname`.


  ## Example


  ### Before


  ```typescript

  import { useRouter } from 'next/router';


  function Component() {
  	const { query } = useRouter();
  	const { a, b, c } = query;
  }

  ```


  ### After


  ```typescript

  import { useParams, useSearchParams } from 'next/navigation';

  import { useCallback } from 'react';


  function Component() {
  	const params = useParams();
  	const searchParams = useSearchParams();
  	const getParam = useCallback(
  		(p: string) => params?.[p] ?? searchParams?.get(p),
  		[params, searchParams],
  	);

  	const a = getParam('a');
  	const b = getParam('b');
  	const c = getParam('c');
  }

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/replace-next-router
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=-wqkAQr7ILgYeTRozWTEgiUvmSY
f_cli-command: deepcode next/13/replace-next-router
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 13.4.
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Replace Next Router
updated-on: 2023-11-30T17:10:02.988Z
published-on: 2023-11-30T17:10:02.994Z
f_slug-name: replace-next-router
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T17:10:02.999Z
seo:
  title: Next.js Replace Next Router | Deepcode Automations
  og:title: Next.js Replace Next Router | Deepcode Automations
  twitter:title: Next.js Replace Next Router | Deepcode Automations
  description: This automation allows you to migrate the `useRouter` hook to the new
    `useRouter` hook imported from `next/navigation`.
  twitter:card: This automation allows you to migrate the `useRouter` hook to the new
    `useRouter` hook imported from `next/navigation`.
  og:image: /assets/images/replace-next-router.jpg
---
This automation allows you to migrate the `useRouter` hook to the new `useRouter` hook imported from `next/navigation`.