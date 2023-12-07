---
created-on: 2023-11-29T16:55:21.254Z
f_long-description: >-
  The first step to migrate your pages to the `app` directory is to provide a
  new file structure, respected by the App router.


  This is attempted by this codemod, which reads the contents of your `pages` directory and creates the placeholder files.


  The placeholder files define the basic layout and page structure.


  The boilerplate includes the following:


  * placeholder `page.tsx` and `layout.tsx` files which define a UI unique to a route.

  * the placeholder `app/layout.tsx` file which replaces `pages/_app.tsx` and `pages/_document.tsx` files.

  * the placeholder `error.tsx` file which replaces `pages/_error.tsx` files.

  * the placeholder `not-found.tsx` file which replaces `pages/404.tsx` files.


  If the codemod detects that a `getStaticProps` function is not used, it will be removed. Otherwise, it will remove the `export` keyword from the function definition.


  ## Example


  If you have the following directory:


  ```markdown
    pages
    ├── _app.tsx
    ├── _document.tsx
    ├── _error.tsx
    ├── 404.tsx
    ├── a.tsx
    └── b
          └── c.tsx
  ```


  The codemod will generate the following corresponding directory:


  ```markdown
    app
    ├── page.tsx
    ├── layout.tsx
    ├── error.tsx
    ├── not-found.tsx
    ├── a
          └── page.tsx
    └── b
          └── c
                └── page.tsx
  ```


  ## Links for more info


  * [App Router Migration Guide | Vercel](https://nextjs.org/docs/app/building-your-application/upgrading/app-router-migration)
f_github-link: https://github.com/deepcode-ai/codemod-registry/tree/main/codemods/next/13/app-directory-boilerplate
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=QKEdp-pofR9UnglrKAGDm1Oj6W0
f_cli-command: deepcode next/13/app-directory-boilerplate
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 13.4.
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js App Directory Boilerplate
updated-on: 2023-11-29T16:55:21.259Z
published-on: 2023-11-29T16:55:21.274Z
f_slug-name: app-directory-boilerplate
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-29T16:55:21.281Z
seo:
  title: Next.js App Directory Boilerplate | Deepcode Automations
  og:title: Next.js App Directory Boilerplate | Deepcode Automations
  twitter:title: Next.js App Directory Boilerplate | Deepcode Automations
  description: This automation helps you migrate to the Next.js app directory by
    reading the contents of your `pages` directory and creates the placeholder
    files.
  twitter:card: This automation helps you migrate to the Next.js app directory by
    reading the contents of your `pages` directory and creates the placeholder
    files.
  og:image: /assets/images/app-directory-boilerplate-codemod.jpg
---
This automation reads the contents of your `pages` directory and creates the placeholder files.