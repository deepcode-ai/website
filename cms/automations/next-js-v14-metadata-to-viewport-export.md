---
created-on: 2023-12-01T15:50:10.515Z
f_long-description: >-
  ## Description


  This codemod migrates certain viewport metadata to `viewport` export.


  ## Example


  ### Before


  ```typescript

  export const metadata = {
  	title: 'My App',
  	themeColor: 'dark',
  	viewport: {
  		width: 1,
  	},
  };

  ```


  ### After


  ```typescript

  export const metadata = {
  	title: 'My App',
  };


  export const viewport = {
  	width: 1,
  	themeColor: 'dark',
  };

  ```


  ## Links for more info


  * [Next.js V14 Upgrade](https://nextjs.org/docs/pages/building-your-application/upgrading/version-14)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/14/metadata-to-viewport-export
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=hCw9Zucqpf__QgZRCVDUvzSMdeE
f_cli-command: deepcode next/14/metadata-to-viewport-export
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 14.
f_verified-codemod: true
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js V14 - Metadata to Viewport Export
updated-on: 2023-12-01T15:50:10.530Z
published-on: 2023-12-01T15:50:10.540Z
f_slug-name: metadata-to-viewport-export
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-v13-to-v14-upgrade.md
tags: automations
date: 2023-12-01T15:50:10.547Z
seo:
  title: Next.js v14 Metadata to Viewport Export | Deepcode Automations
  og:title: Next.js v14 Metadata to Viewport Export | Deepcode Automations
  twitter:title: Next.js v14 Metadata to Viewport Export | Deepcode Automations
  description: This automation migrates certain viewport metadata to `viewport` export.
  twitter:card: This automation migrates certain viewport metadata to `viewport` export.
  og:image: /assets/images/next-og-import.jpg
---
This automation migrates certain viewport metadata to `viewport` export.