---
created-on: 2023-11-30T15:56:24.605Z
f_long-description: >-
  ## Description


  This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules.


  ## Example


  ### Before


  ```typescript

  const Head = () => {
  	return (
  		<head>
  			<style type="text/css">
  				{`
          body {
            margin: 0;
            padding: 0;
          }
        `}
  			</style>
  		</head>
  	);
  };


  export default Head;

  ```


  ### After


  The file gets transformed into:


  ```typescript

  import styles from 'Head.module.css';


  const Head = () => {
  	return <head className={styles['wrapper']}></head>;
  };


  export default Head;

  ```


  And the codemod creates the new file `Head.module.css` which contains:


  ```css

  body {
  	margin: 0;
  	padding: 0;
  }

  ```


  ### Links for more info


  * [Next.js - CSS in JS](https://nextjs.org/docs/pages/building-your-application/styling/css-in-js)
f_github-link: https://github.com/deepcode-ai/codemod-registry/blob/main/codemods/next/13/move-css-in-js-styles
f_vs-code-link: vscode://deepcode.deepcode-vscode-extension/showCodemod?chd=fPpa1xqB9D0AN4VazhrRkrWri9g
f_cli-command: deepcode next/13/move-css-in-js-styles
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13.4
f_verified-codemod: true
f_author: cms/authors/deepcode.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Move CSS in JS Styles
updated-on: 2023-11-30T15:56:24.615Z
published-on: 2023-11-30T15:56:24.627Z
f_slug-name: comment-deletable-files
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T15:56:24.633Z
seo:
  title: Next.js Move CSS in JS Styles | Deepcode Automations
  og:title: Next.js Move CSS in JS Styles | Deepcode Automations
  twitter:title: Next.js Move CSS in JS Styles | Deepcode Automations
  description: This is a highly experimental codemod that moves the CSS-in-JS
    styles into the CSS Modules.
  twitter:card: This is a highly experimental codemod that moves the CSS-in-JS
    styles into the CSS Modules.
  og:image: /assets/images/move-css-in-js-styles.jpg
---
This is a highly experimental codemod that moves the CSS-in-JS styles into the CSS Modules.