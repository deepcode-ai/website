---
created-on: 2023-11-30T16:07:44.129Z
f_long-description: >-
  # New Image Experimental


  ## Description


  This codemod **dangerously** migrates the usages of the `Image` component from the `next/legacy/image` module to the `next/image` module.

  This is achieved by adding inline styles and removing unused props.


  Please note this codemod is experimental and only covers static usage (such as `<Image src={img} layout="responsive" />`) but not dynamic usage (such as `<Image {...props} />`).


  Functionality:


  * Removes `layout` prop and adds `style`

  * Removes `objectFit` prop and adds `style`

  * Removes `objectPosition` prop and adds `style`

  * Removes `lazyBoundary` prop

  * Removes `lazyRoot` prop

  * Changes next.config.js `loader` to "custom", removes `path`, and sets `loaderFile` to a new file.


  ## Examples


  ### Before: intrinsic


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  function Page() {
  	return <Image src={img} />;
  }

  ```


  ### After: intrinsic


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  const css = { maxWidth: '100%', height: 'auto' };

  function Page() {
  	return <Image src={img} style={css} />;
  }

  ```


  ### Before: responsive


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  function Page() {
  	return <Image src={img} layout="responsive" />;
  }

  ```


  ### After: responsive


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  const css = { width: '100%', height: 'auto' };

  function Page() {
  	return <Image src={img} sizes="100vw" style={css} />;
  }

  ```


  ### Before: fill


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  function Page() {
  	return <Image src={img} layout="fill" />;
  }

  ```


  ### After: fill


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  function Page() {
  	return <Image src={img} sizes="100vw" fill />;
  }

  ```


  ### Before: fixed


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  function Page() {
  	return <Image src={img} layout="fixed" />;
  }

  ```


  ### After: fixed


  ```typescript

  import Image from 'next/image';

  import img from '../img.png';


  function Page() {
  	return <Image src={img} />;
  }

  ```


  ### Links for more info


  * [Next Image Experimental](https://nextjs.org/docs/pages/building-your-application/upgrading/codemods#next-image-experimental)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/new-image-experimental
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=oU68MgnhDvq08nBVNTQK8fouqGI
f_cli-command: deepcode next/13/new-image-experimental
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13.4
f_verified-codemod: false
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js New Image Experimental
updated-on: 2023-11-30T16:07:44.136Z
published-on: 2023-11-30T16:07:44.144Z
f_slug-name: new-image-experimental
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T16:07:44.151Z
seo:
  title: Next.js New Image Experimental | Deepcode Automations
  og:title: Next.js New Image Experimental | Deepcode Automations
  twitter:title: Next.js New Image Experimental | Deepcode Automations
  description: This automation dangerously migrates the usages of the Image component
    from the next/legacy/image module to the next/image module.
  twitter:card: This automation dangerously migrates the usages of the Image
    component from the next/legacy/image module to the next/image module.
  og:image: /assets/images/new-image.jpg
---
This automation **dangerously** migrates the usages of the `Image` component from the `next/legacy/image` module to the `next/image` module.