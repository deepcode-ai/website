---
created-on: 2023-11-30T17:02:33.725Z
f_long-description: >-
  ## Description


  Generates a static metadata object based on meta tags managed by `next/head`.


  The codemod checks all the child components used in a page file and extracts all the meta tags defined within the `<Head>` component. Such tags are then moved to the very page file alongside the dependencies of the tags.


  ## Example:


  ### Before:


  ```typescript

  // a page file

  import Meta from '../../components/a.tsx';
  	export default function Page() {
  		return <Meta />;
  }


  // component file

  import Head from 'next/head';

  import NestedComponent from '../components/b.tsx';

  export default function Meta() {
  	return (<>
  	<Head>
  		<title>title</title>
  	</Head>
  	<NestedComponent />
  	</>)
  }


  // nested component file

  import Head from 'next/head';


  export default function NestedComponent() {
  	return <Head>
  	<meta name="description" content="description" />
  	</Head>
  }


  export default NestedComponent;

  ```


  ### After:


  ```typescript

  // page file

  import { Metadata } from 'next';

  import Meta from '../../components/a.tsx';

  export const metadata: Metadata = {
  	title: `title`,
  	description: 'description',
  };

  export default function Page() {
  	return <Meta />;
  }

  ```


  ### Links for more info


  * [App Router Upgrade - Migrating Next Head](https://nextjs.org/docs/app/building-your-application/upgrading/app-router-migration#step-3-migrating-nexthead)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/replace-next-head
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=HCouE4WzwvH-jcfOJ3xYLz4YaTA
f_cli-command: deepcode next/13/replace-next-head
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13.
f_verified-codemod: true
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Replace Next Head
updated-on: 2023-11-30T17:02:33.740Z
published-on: 2023-11-30T17:02:33.746Z
f_slug-name: replace-next-head
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T17:02:33.753Z
seo:
  title: Next.js Replace Next Head | Deepcode Automations
  og:title: Next.js Replace Next Head | Deepcode Automations
  twitter:title: Next.js Replace Next Head | Deepcode Automations
  description: This automation generates a static metadata object based on meta tags
    managed by `next/head`.
  twitter:card: This automation generates a static metadata object based on meta tags
    managed by `next/head`.
  og:image: /assets/images/replace-next-head.jpg
---
This automation generates a static metadata object based on meta tags managed by `next/head`.