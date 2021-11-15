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

- Micro-Front-End Strategy
  - Several people use this to leverage a small front end to support their legacy or other tooling

### Build an App

- Built in TypeScript
- Built in Next.js
- We're going to build an app to register for a convention

### Good Accessibility

- Don't use divs everywhere!
  - Good accessibility needs to have limited tags
  - [Cory's Tweet](https://twitter.com/housecor/status/1434168409072324610)
- h1 tags are big time important for accessibility and search engine optimization
- run a screen reader on your app to see how accessible it is for people who can not see
- Improving accessibility improves the developer experience as well because you have more specificity in your tag

### Forms

- What is the least amount of state that I can store?
  - "Don't put anything in state that could be derived from existing state"
    - `const firstName = "Cory";`
    - `const lastName = "House";`
    - `const fullName = "Cory House";`
    - Now you have to remember to update multiple things in state while it could be derived
  - If it's expensive, throttle it, memoize it, lazy load it
    - Calculate it on each render, do not use state to store dat

[This session in a tweet form](https://twitter.com/housecor/status/1437765667906854915?lang=en)

### Eight Ways to Handle State in React Apps

- URL
- Web Storage
  - putting items in a cart
- Local State
- Lifted State
- Derived State
- Refs
  - useful for state that I don't need to render, like an instance variable in OOP
- Context
  - Overused in my opinion (Redux is overused)
- Third Party Library
  - Consider a 3rd party library for state

[image with definitions](https://twitter.com/housecor/status/1437765673439088644/photo/1)

- Two kinds of forms
  - Controlled Form
  - Uncontrolled Form - Use refs to grab the data out of the markup

### Back to Forms

- When you build a form what sorts of things to put in state
  - Whether it's dirty
    - When a field has been editted
    - Disable the submit button
  - Validation Errors
  - Server Side Validation - Check for existing user
  - Input Masking
  - Dates
  - Whether the form has been submitted or not
- You don't need a form library, you need a pattern - What State Do We Need?
  - [image](https://twitter.com/housecor/status/1437765736026542081/photo/1)
  - Store as "touched"
    - touched: What fields have been touched?
  - Store as "status"
    - submitted: Has the form been submitted?
    - isSubmitting: Is a form submission in progress?
  - Derive
    - isValid: Is the form currently valid?
    - errors: What are the errors for each field?
    - dirty: Has the form changed?
- Finite State Machine - programmatically enforce that you can only be in one state at a time, and you are only allowed to shift to certain states from the current state
  - State Enums
    - [image](https://twitter.com/housecor/status/1437765743177777157/photo/1)
  - When you think about finite states, it will make your forms and code much easier to understand
  - "Is there a way for me to enforce that the impossible can not occur?"
- Uncontrolled Forms - "Reactland is a paradigm that doesn't look like jQuery"
- Class based components are dead
  - react-error-boundary - fixes on gap from class based components
  - React is moving towards not even having a class based component docs
- One of the nicest things about TypeScript over JavaScript is you don't need to declare the import statements anymore. You can just lean on the compiler!
- HTML - name is usually redundant if you can lean on id
- I had strong opinions on semicolons, quotes, etc... There is no startup in silicon value that failed because of these things. Use prettier.

### TDD - Jest and Cypress

- "I use jest for unit testing and I use cypress for everything else."
- `npm i jest ts-jest cypress @testing-library/react @testing-library/cypress start-server-and-test npm-run-all`
- Cypress - try to run it once, then try to run it again
- Cypress is about to radically improve their story about unit-testing and they will be rolling things out next year
- start server and test npm package
  - https://www.npmjs.com/package/start-server-and-test
    "cy": "start-server-and-test dev http://localhost:3000 cy-open",
  - Runs the cypress along with the server
  - Cypress should be validating what my form should expect instead of me (being human) trying to work it out
- Testing Library
  - https://testing-library.com/docs/
    - cypress needed import - https://testing-library.com/docs/cypress-testing-library/intro
- Code to make Cypress fill out the form!

```js
/// <reference types="cypress" />

it("should render form", () => {
  cy.visit("http://localhost:3000");
  cy.findByLabelText("Title").type("React Intro");
  cy.findByLabelText("Abstract").type("Intro to React.");
});
```

- In Cypress the assertions are implied, you don't need the explicit assert and expect terms
- The reason you choose the form to submit the form is that you can hit the enter key to submit as opposed to being forced to click the button to submit the values
- Using declared functions versus arrow functions lets you leverage hoisting of functions better
- In jsx whenever you add curly braces think, "I want to write JavaScript now"

- Why use a union type over using enums

  - https://stackoverflow.com/questions/40275832/typescript-has-unions-so-are-enums-redundant
  - Specific response - https://stackoverflow.com/a/60041791

- In Cypress you can do several testing within the same tests because it's all abstracted and documented within itself
- Brilliant thought: (Code Complete) using a return early in code you don't have to do as many conditionals to prevent other actions and it will clean up a lot of redundancies and be a lot more readable.
- Fun stuff, remember to have a unique key for every item mapped over in react
- With this workflow you never have to handle inputting all the information in the forms, cypress just takes care of it for you. It's absolutely wonderful!

- I would choose Cypress over Jest for comprehensive testing

### json-server

[json-server](https://github.com/typicode/json-server)
Get a full fake REST API with zero coding in less than 30 seconds (seriously)

### 35+ Ways To Handle State?!

[Old blog post](https://www.bitnative.com/2020/06/19/30-ways-to-handle-react-state/)

**React**

- class state
- useState
- useReducer
- Refs
  - Don't do this very often
- Context
  - Do not put form state information into context
  - Can also store functions as well
  - It's a good idea to put a wrapper around it so you can use it via hooks (Provider wrapper)
- Lifted
  - Whenever the components need to share state, you can lift the state up through the chain (instead of having to only pass down props)
- Derived
  - Took existing state and calculated from it
  - Just JavaScript calculations simply running in a function
  - Avoid setting state when just deriving it can suffice

**Web Platform**

- JS global
- DOM
  - This can be the source of truth if you're handling uncontrolled components
- URL
- Cookie
- localStorage
  - https://usehooks.com/useLocalStorage/
  - utilizes an open source hook on useHooks.com
- sessionStorage

**Third Party**

- Redux
  - Not really super useful and necessary anymore. Probably better using react-query or swr.
- Mobx
- Recoil
- react-query
  - Top of his list for utilizing state management (Despite the fact that his Redux tutorial series is his most popular)
- swr
- Relay
- Apollo
  - If you're working in GraphQL this is wonderful
- Immer
  - RTK uses Immer
  - https://github.com/immerjs/immer
    - Write mutable code that's actually immutable
  - If you freeze an object, it actually will enforce it
- Immutable.js
- Formik
- React Hook Form
- Mobx-state-tree
- mobx-react-lite
- Easy-peasy
- Overmindjs
- react-easy-state
- Effector
- react-sweet-state
- Freezer
- Undux
- Statux
- zustand
- Reatom
- Jotai

- RTK Query Overview - also mentioned as another alternative during the discussion but not in the slideshow
- Abstractions are useful, but most abstractions leak at some point. It has quirks, it has faults, you can't lean on it perfectly.
- If you're using excess tools then you will be dealing with the "weird" instead of dealing with the core React issues.

### Prop Drilling

- Prop drilling - the problem of passing props down through many layers when some components do not even need the state/props
  - You can use component composition to solve the problem, a design implementation solution
    - https://overreacted.io/before-you-memo/
    - Great dan abramov blog discussing the design and way that the rerendering process can clunkily slow things down
    - 2 ways to avoid this
      - Moving the state down
        - You can take the expensive stuff and move it over
      - when you set the props as children, then it won't rerender the children content unnecessarily
  - Although, once you're in multiple components, Redux and Context is perfectly fine and a good use case

### Using Github editor

- Hit period inside of the repository on Github and it will open up VSCode within GitHub in the repository

### When does React render

- state change
- props change
- when context changes

### How to avoid React renders

- use memo
- use ref
- "Only pass the things to your component that they actually need. The principal of least privilege!"
  - Need to work on this in our code base for work!!

### If you have a lot of Performance Problems in React, then it's most likely a design issue

- You notice that Google paginates - 25 records or so?
- You don't need to show so much information all at once!
  - This might be a good use case to swap back plan data queries instead of placing plan data in state. Could be expensive re-renders...

### Coding by Contract

- Think of my jsx as coding by contract
  - return early

### Custom Hooks

- If you have the same structural functionality then you can have the hook trigger a much more simplified call
  - showed this [image](https://twitter.com/housecor/status/1437765709849927684)
    - but don't use this! use react-query!
    - [example code](https://github.com/coryhouse/managing-react-state-kcdc-2021/blob/master/src/services/useFetch.js)

### React-Query

- Extremely simplifies the pulls of data from the api
- [Link](https://react-query.tanstack.com/)

Side Note: Multiple times Cory mentioned the "sad souls that are still using class components"

### X-State

- I rarely find that I'm building something that is complicated enough to merit utilizing x-state
- Although it is very powerful, and a very good tool for complex situations where finite state machines will be very useful

### 7 Years of Lessons Learned

reactjsconsulting.com

1. Know the 8 ways to handle state, and when to consider each.
2. Class components are dead.
3. "Normalize" state bby deriving on render.
4. Understand when React renders, and how to avoid it.
5. Most state is remote state. (see remote state maturity model).
6. Start local, then lift. Global is a last resort. Prop drilling is no biggie.
7. Wrap context in a single file.
   1. https://github.com/coryhouse/managing-react-state-kcdc-2021/blob/master/src/cartContext.js
   2. Example of wrapping the context to prevent other things from manipulating or messing with it.
8. Embrace immutable JS features. You don't need LoDash, Underscore, Ramda.
9. You don't need a form library. You need a pattern.
10. State Enums are fire. You likely don't need XState and state charts.
11. PropTypes are dead. Long live TypeScript.
12. Start with controlled forms. You'll end up needing the flexibility.
13. Context/Redux/etc. are overused. Remote state is common. Global state is rare.
14. When JSX feels messy/constraining, return early, or extract a func / component.
15. Consider useReducer when state complexity warrants isolated tests.

- I would lean towards using one solution for solving state management, because it will be too confusing to manage different tooling to store the information in multiple places.

  - Redux devtools are sweet when compared with Context

- In Hooks - React knows what the state was on the previous render, so it injects the previous value again on rerender

### Last Minute Tips

- https://eslint.org/docs/rules/no-restricted-imports
  - not allow certain imports
- alphabatize props - easier to read and see, can set it up via eslint
- set up rules with eslint in jest, cypress or typescript
-
