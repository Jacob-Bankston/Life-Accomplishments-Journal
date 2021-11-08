# Lessons Learned From 7 Years in React

## Cory House

### Description

This workshop explores a long list of lessons learned from working in React for the last 7 years. Tips include rethinking separation of concerns, selecting state management approaches, types vs propTypes, performance optimizations, form optimizations, novel workflows, utilizing mock APIs, automated testing strategies, and patterns for sharing components.

### What We're Doing Today

Coding!

### Thoughts

- Create React App takes a while to load and run
- Create React App has a full time staff at Facebook, and it doesn't really move that quickly
- Next.js release notes spins out so fast, they continuously are improving and refining their process
- Feel like create-react-app will potentially fall out of favor in 2022
- Astro Build is super compelling, Veet, Next, and Gatsby are all great starters for React
  - Better seo from astro.build
  - Still not at a 1.0 version, so not recommending yet
- We know React 18 is coming, and it is going to give us "Server-Side Components"
  - Server components are being designed alongside popular community groups like Next.js
- The days of reaching for create-react-app as a foregone conclusion may be moving away from us
- It's interesting that Gatsby is starting to do the things that Next.js does
- Cory made react-slingshot years ago and there wasn't a starter template - don't use it

### Next.js

- It's not the most obvious alternative, but it is the most popular alternative
- MUCH more active development

  - SEE PICTURE

- BFF (Back-end for Front-end), you end up creating a back end that calls all the apis you need to call.

  - Set your session as an auth token as an http-only cookie, so javascript can not read it
  - You create a back end for the front end. It creates the cookie, and sends it back and forth.
  - You can create an api call that gives exactly what you want back
  - You can eliminate the multiple calls to the api by refining what information you precisely want

- New Recommendation by 0Auth - You do not want to store a "jot" in a cookie that is readable
- Originally built a current project with Express.js as the back-end for the front-end, and realized that Next.js would have been a perfect use case for his situation

- Next.js has strong opinions about where you put stuff

  - In Next if you want to set headings, you do that on the page itself
  - Changes the tag when you click the url
  - In Next.js you convey the routes by the file folder system - Ruby on Rails popularized this convention over code
  - Image, Styling, Routes and API calls all normalized with their setup
  - "getStaticProps" function only runs on the server - I can write a function on a component that only runs on a server

- Pretty much everyone is using lazy-loading and everyone is using react-router
- When you load the page, Next.js will load up the pages that are in links on the page "eager loading"

### Why TypeScript is now good

- babel now supports TypeScript
- react now supports TypeScript

### Compelling Options

- [List](https://github.com/coryhouse/reactjsconsulting/issues/47)
- create-react-app, Vite
- Server-rendered, no DB included: Next, Remix, Gatsby, After [Compare Vid](https://www.youtube.com/watch?v=dfMhRYOtglg)
- Server-rendered, DB included: Redwood (GraphQL and Prisma), Blitz

[Have Single-Page Apps Ruined the Web? | Transitional Apps with Rich Harris, NYTimes](https://www.youtube.com/watch?v=860d8usGC0o)

- Maintainer of Svelte
