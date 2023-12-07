---
created-on: 2023-11-30T16:16:11.454Z
f_long-description: >-
  ## Description


  Safely removes `<a>` from `Link` components imported from the `next/link` module or adds the `legacyBehavior` prop on the component level.


  ## Example


  ### Before


  ```typescript

  export default function Component() {
  	return (
  		<Link href="/a">
  			<a>Anchor</a>
  		</Link>
  	);
  }

  ```


  ### After


  ```typescript

  export default function Component() {
  	return <Link href="/a">Anchor</Link>;
  }

  ```


  ### Links for more info


  * [Next.js App Router Migration - New Link](https://nextjs.org/docs/pages/building-your-application/upgrading/codemods#new-link)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/new-link
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=lhVaxNlJkzNgtD-kgO09P1GPXKg
f_cli-command: deepcode next/13/new-link
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13
f_verified-codemod: true
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js New Link
updated-on: 2023-11-30T16:16:11.465Z
published-on: 2023-11-30T16:16:11.472Z
f_slug-name: new-link
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T16:16:11.479Z
seo:
  title: Next.js New Link | Deepcode Automations
  og:title: Next.js New Link | Deepcode Automations
  twitter:title: Next.js New Link | Deepcode Automations
  description: This automation safely removes <a> from Link components imported
    from the next/link module or adds the legacyBehavior prop on the component
    level.
  twitter:card: This automation safely removes <a> from Link components imported
    from the next/link module or adds the legacyBehavior prop on the component
    level.
  og:image: /assets/images/new-link.jpg
---
This codemod safely removes `<a>` from `Link` components imported from the `next/link` module or adds the `legacyBehavior` prop on the component level.
