---
created-on: 2023-12-01T15:31:50.031Z
f_long-description: >-
  ## Description


  This codemod moves transforms imports from `next/server` to `next/og` for usage of [Dynamic OG Image Generation](https://nextjs.org/docs/app/building-your-application/optimizing/metadata#dynamic-image-generation).


  ## Example


  ### Before


  ```typescript

  import { ImageResponse } from 'next/server';

  ```


  ### After


  ```typescript

  import { ImageResponse } from 'next/og';

  ```


  ## Links for more info


  * [Next.js V14 Upgrade](https://nextjs.org/docs/pages/building-your-application/upgrading/version-14)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/14/next-og-import
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=YH4iWtje8EfAlF0_ywnKrKTrQJY
f_cli-command: deepcode next/14/next-og-import
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 14.
f_verified-codemod: true
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js V14 - Next OG Import
updated-on: 2023-12-01T15:31:50.040Z
published-on: 2023-12-01T15:31:50.053Z
f_slug-name: next-og-import
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-v13-to-v14-upgrade.md
tags: automations
date: 2023-12-01T15:31:50.060Z
seo:
  title: Next OG Import Automation | Deepcode Automations
  og:title: Next OG Import Automation | Deepcode Automations
  twitter:title: Next OG Import Automation | Deepcode Automations
  description: This automation transforms imports from `next/server` to `next/og`
    for the usage of Dynamic OG Image Generation.
  twitter:card: This automation transforms imports from `next/server` to `next/og`
    for the usage of Dynamic OG Image Generation.
  og:image: /assets/images/next-og-import.jpg
---
This automation transforms imports from `next/server` to `next/og` for the usage of Dynamic OG Image Generation.