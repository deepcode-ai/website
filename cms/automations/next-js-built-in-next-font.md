---
created-on: 2023-11-29T17:16:01.786Z
f_long-description: >-
  ## Description


  This codemod transforms the module specifier `@next/font/*` in import statements into `next/font/*`.


  Using the `@next/font/*` modules is deprecated since Next.js v13.2.


  ## Example


  ### Before


  ```typescript

  import { Inter } from '@next/font/google';

  ```


  ### After


  ```typescript

  import { Inter } from 'next/font/google';

  ```


  ## Links for more info


  * [App Router Migration Guide - Built-in Font | Vercel](https://nextjs.org/docs/pages/building-your-application/upgrading/codemods#use-built-in-font)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/next/13/built-in-next-font
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=USN0ETTSbUY-j1UV3DjYcjLtzvU
f_cli-command: deepcode next/13/built-in-next-font
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 13.4.
f_verified-codemod: true
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Built in Next Font
updated-on: 2023-11-29T17:16:01.799Z
published-on: 2023-11-29T17:16:01.808Z
f_slug-name: built-in-next-font
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 30 seconds/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-29T17:16:01.817Z
seo:
  title: Next.js Built In Font | Deepcode Automations
  og:title: Next.js Built In Font | Deepcode Automations
  twitter:title: Next.js Built In Font | Deepcode Automations
  description: This automation helps you migrate to the Next.js app directory by
    transforming the module specifier `@next/font/*` in import statements into
    `next/font/*`.
  twitter:card: This automation helps you migrate to the Next.js app directory by
    transforming the module specifier `@next/font/*` in import statements into
    `next/font/*`.
  og:image: /assets/images/built-in-font-codemod.jpg
---
This automation transforms the module specifier `@next/font/*` in import statements into `next/font/*`.