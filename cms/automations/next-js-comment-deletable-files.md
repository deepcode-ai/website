---
created-on: 2023-11-30T15:47:23.714Z
f_long-description: >-
  ## Description


  This codemod is recommended when migrating from the `/pages` to the `/app` directory.


  It adds a comment to files that should be deleted and migrated to different files during the migration process.


  Namely, such are the following files:


  * `_document.*`,

  * `_app.*`,

  * `_error.*`.


  ## Example


  ### Before


  ```typescript

  import 'highlight.js/styles/default.css';

  import 'swagger-ui-react/swagger-ui.css';


  import '../styles/globals.css';


  function MyApp({ Component, pageProps }) {
  	return <Component {...pageProps} />;
  }


  export default MyApp;

  ```


  ### After


  ```typescript

  /*This file should be deleted. Please migrate its contents to appropriate files*/

  import 'highlight.js/styles/default.css';

  import 'swagger-ui-react/swagger-ui.css';


  import '../styles/globals.css';


  function MyApp({ Component, pageProps }) {
  	return <Component {...pageProps} />;
  }


  export default MyApp;

  ```
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/comment-deletable-files
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=BaHE4pik14OhABrBRaAUohzhcs0
f_cli-command: deepcode next/13/comment-deletable-files
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13.4
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Comment Deletable Files
updated-on: 2023-11-30T15:47:23.729Z
published-on: 2023-11-30T15:47:23.739Z
f_slug-name: comment-deletable-files
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T15:47:23.748Z
seo:
  title: Next.js Comment Deletable Files | Deepcode Automations
  og:title: Next.js Comment Deletable Files | Deepcode Automations
  twitter:title: Next.js Comment Deletable Files | Deepcode Automations
  description: This automation helps you migrate to the Next.js app directory by
    transforming the module specifier `@next/font/*` in import statements into
    `next/font/*`.
  twitter:card: This automation helps you migrate to the Next.js app directory by
    transforming the module specifier `@next/font/*` in import statements into
    `next/font/*`.
  og:image: /assets/images/comment-deletable-files.jpg
---
This automation is recommended when migrating from the `/pages` to the `/app` directory.