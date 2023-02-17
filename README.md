# Linaria Proof of Concept
This repo contains a small proof of concept monorepo NextJS application with integrated Component Library support and TypeScript. The idea of this POC is to show major architecture improvements to a code base to allow the Component Library to scale with multiple site setups with less performance overhead and a better developer experience.

## Goals

- _Developer Confidence:_ Less bugs, conflicts and complexities
- _Less Overhead:_ Reduce unnecessary complications due to architecture restrictions
- _Scalability:_ New sites can be spun up by just updating theme configurations, components can be extended as and when needed.
- _Design Alignment:_ Designs in Figma go hand in hand with Design Tokens that enforce consistency
- _Simplification:_ Components require less bootstrapped code

## Dependencies
- [NextJS v13](https://nextjs.org/blog/next-13-1)
- [React 18](https://reactjs.org/blog/2022/03/29/react-v18.html)
- [StoryBook 6](https://storybook.js.org/blog/storybook-6-0/)
- [Monorepo's](https://monorepo.tools/)
- [TypeScript](https://www.typescriptlang.org/)

## Features

- Linaria: is a Zero-runtime CSS in JS library. This means we can leverage the benefits of CSS-in-JS without the performance overhead.
- Better Code Coverage: The site only loads CSS if a component is rendered on the page
- Support for locally-scoped and globally-scoped CSS rules
- Supports CriticalCSS using SSR
- Much like CSS Modules, styles are scoped, meaning specificity and importance issues and bleeding CSS styles are a thing of the past.

## Compatibility

- [x] Works with StyleLint?
- [x] Works with VSCode?
- [x] Can leverage CSS Preprocessors?
- [x] Extendable?
- [x] Theme-able?
- [x] Supports CSS Source maps?
- [x] Integrated with Design Tokens
- [x] Can be integrated with TypeScript

## Benefits

<details>
  <summary>Is this architecture performant?</summary>
  
  Yes, most CSS-in-JS solutions in the current space provide closer integration with Components, however the CSS is included in the JS bundle sizes, creating bloated bundles that are difficult to slim down. Linaria lets you write and reap all the developer benefits of CSS-in-JS but all CSS is extracted at build time into CSS files which can be loaded asynchronously with the JavaScript files themselves.
</details>

<details>
  <summary>Is the CSS scalable across multiple projects?</summary>
  
  Yes, the nature of CSS-in-JS means that CSS is encapsulated within actual React Components. Linaria provides API's to scale, extend, interpolate and theme components in a manner which does not add extra overhead or complicate developer experience. 
</details>

<details>
  <summary>Can we easily extend components safely, securely and without domino effects?</summary>
  
  Yes, all CSS rules written are scoped to the component, this means that CSS can not bleed across other components across the site. Global and Local CSS can also be declared to ensure saftey. Whats more, is each CSS ruleset can be typed, using interfaces to ensure that engineers do not and cannot extend items which should not be allowed to be extended.
</details>

## Incremental Adoption
