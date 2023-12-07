---
created-on: 2023-11-30T16:26:21.088Z
f_long-description: >-
  ## Description


  This codemod safely migrates existing Next.js 10, 11, 12 applications importing `next/image` to the renamed `next/legacy/image` import in Next.js 13 by replacing `next/image` imports with `next/legacy/image` and replacing `next/future/image` imports with `next/image`.


  ## Example


  ### Before


  ```typescript

  import Image from 'next/image';

  import FutureImage from 'next/future/image';


  export default function Home() {
  	return (
  		<div>
  			<Image src="/test.jpg" width="100" height="200" />
  			<FutureImage src="/test.png" width="300" height="400" />
  		</div>
  	);
  }

  ```


  ### After


  ```typescript

  import Image from 'next/legacy/image';

  import FutureImage from 'next/image';


  export default function Home() {
  	return (
  		<div>
  			<Image src="/test.jpg" width="100" height="200" />
  			<FutureImage src="/test.png" width="300" height="400" />
  		</div>
  	);
  }

  ```


  ### Links for more info


  * [App Router Upgrade - Next Image to Legacy Image](https://nextjs.org/docs/pages/building-your-application/upgrading/codemods#next-image-to-legacy-image)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/next-image-to-legacy-image
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=3eSpQRdmwHQuXlyNEsZcdbx5Q10
f_cli-command: deepcode next/13/next-image-to-legacy-image
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13
f_verified-codemod: true
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Next Image to Legacy Image
updated-on: 2023-11-30T16:26:21.095Z
published-on: 2023-11-30T16:26:21.104Z
f_slug-name: next-image-to-legacy-image
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T16:26:21.114Z
seo:
  title: Next Image to Legacy Image | Deepcode Automations
  og:title: Next Image to Legacy Image | Deepcode Automations
  twitter:title: Next.js New Link | Deepcode Automations
  description: This automation safely migrates existing Next.js 10, 11, 12
    `next/image` imports to their corresponding imports in Next.js 13.
  twitter:card: This automation safely migrates existing Next.js 10, 11, 12
    `next/image` imports to their corresponding imports in Next.js 13.
  og:image: /assets/images/next-image-to-legacy-image.jpg
---
This automation safely migrates existing Next.js 10, 11, 12 `next/image` imports to their corresponding imports in Next.js 13.
