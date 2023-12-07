---
created-on: 2023-11-30T16:45:39.847Z
f_long-description: >-
  ## Description


  The following data fetching methods are no longer available in the `app` directory:


  * `getStaticPaths`,

  * `getServerSideProps`,

  * `getStaticProps`.


  The codemod migrates the data fetching functions into the supported in the `app` directory:


  * `getStaticPaths` -> `generateStaticParams`

  * `getServerSideProps` -> `getData`

  * `getStaticProps` -> `getData` (used in the component)


  If the `getStaticPaths` function has only one expression in the return statement, it will be inlined within the `nextData` function, otherwise it will remain unchanged.


  When migrating the `getServerSideProps` functions, the codemod assumes that only the `params` property of the first argument is used.


  It additionally adds types for aforementioned `params` and page props.


  It will also add the `revalidate` and `dynamicParams` route segment properties.


  ## Example


  ### Before


  ```typescript

  import PostLayout from '@/components/post-layout';


  export async function getStaticPaths() {
  	return {
  		paths: [{ params: { id: '1' } }, { params: { id: '2' } }],
  		fallback: 'blocking',
  	};
  }


  export async function getStaticProps({ params }) {
  	const res = await fetch(`https://.../posts/${params.id}`);
  	const post = await res.json();

  	return { props: { post } };
  }


  export default function Post({ post }) {
  	return <PostLayout post={post} />;
  }

  ```


  ### After


  ```typescript

  import { notFound, redirect } from 'next/navigation';

  import PostLayout from '@/components/post-layout';


  type Params = {
  	[key: string]: string | string[] | undefined,
  };


  type PageProps = {
  	params: Params,
  };


  export async function getStaticPaths() {
  	return {
  		paths: [{ params: { id: '1' } }, { params: { id: '2' } }],
  		fallback: 'blocking',
  	};
  }


  export async function generateStaticParams() {
  	return (await getStaticPaths({})).paths;
  }


  export async function getStaticProps({ params }) {
  	const res = await fetch(`https://.../posts/${params.id}`);
  	const post = await res.json();

  	return { props: { post } };
  }


  async function getData({ params }: { params: Params }) {
  	const result = await getStaticProps({ params });

  	if ('redirect' in result) {
  		redirect(result.redirect.destination);
  	}

  	if ('notFound' in result) {
  		notFound();
  	}

  	return 'props' in result ? result.props : {};
  }


  export default async function Post({ params }: PageProps) {
  	const { post } = await getData({ params });

  	return <PostLayout post={post} />;
  }


  export const dynamicParams = true;

  ```


  ### Links for more info


  * [App Router Upgrade - getStaticProps](https://nextjs.org/docs/app/building-your-application/upgrading/app-router-migration#static-site-generation-getstaticprops)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/remove-get-static-props
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=gqDiMZhaiz_RSzyfHeUueiYcGFI
f_cli-command: deepcode next/13/remove-get-static-props
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13.4.
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Migrate Data Fetching Methods
updated-on: 2023-11-30T16:45:39.856Z
published-on: 2023-11-30T16:45:39.865Z
f_slug-name: remove-get-static-props
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 2 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T16:45:39.875Z
seo:
  title: Next.js Migrate Data Fetching Methods | Deepcode Automations
  og:title: Next.js Migrate Data Fetching Methods | Deepcode Automations
  twitter:title: Next.js Migrate Data Fetching Methods | Deepcode Automations
  description: This codemod migrates the data fetching functions into the
    supported in the app directory.
  twitter:card: This codemod migrates the data fetching functions into the
    supported in the app directory.
  og:image: /assets/images/migrate-data-fetching-methods.jpg
---
This automation migrates the data fetching functions into the supported in the `app` directory.