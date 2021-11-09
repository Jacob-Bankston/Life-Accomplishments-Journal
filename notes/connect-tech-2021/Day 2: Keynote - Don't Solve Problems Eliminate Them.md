# Keynote - Don't Solve Problems, Eliminate Them

## Kent C. Dodds

### Description

Humans are natural problem solvers and we're good enough at it that we've survived over the centuries and become the dominant species of the planet. Because we're so good at it, we sometimes become problem seekers too–looking for problems we can solve. Those who most successfully accomplish their goals are the problem eliminators. Let's talk about the distinction between solving and eliminating problems with examples from inside and outside the coding world.

### Links

- TestingJavaScript.com
- kentcdodds.com
- EpicReact.Dev

### Stretches

### Talk #99

### What this talk is

- Problems, Solutions, and Trade-offs

### Thoughts

- Problem Tree
  - Problems lead to solutions lead to problems
- You are problem solvers - Dominant species on the planet
- Before you try to solve the problem, you need to understand what the problem is in the first place
- "Possibly the most common error of a smart engineer iis to optimize the thing that should not exist" - Elon Musk
- Time is a zero sum game
- You should be a problem eliminator
- Solutions hold you captive - the more solutions you build, then your pride and excitement about the solutions make you more invested in continuing to spend time on them
- Tesla is a really awesome case study for problem elimination
- Super fan of hooks - solved so much problems with class based components

### Remix

- Invest in Tesla, you'd be a fool not to be
- Remix would be a replacement for Next.js
  - Nested Routing
  - Seamless Client/Server
    - Remix does a phenomenal job of bridging the gap between the client and server side of things
- We will always have a problem with estimating and specifically underestimating how long something will take to implement
- You can load data and integrate it into state and not have to utilize a useEffect to manage it
- GraphQL is enormous
- everything in Remix just uses web apis
  - the answer for all the docs you can simply look it up on MDN!
- The better you get at Remix, the better you get at the web platform, because it's all based on web apis!
  - fetch Request/Response
  - `<Form />`
  - `<link rel="modulepreload" />`
- "As a JavaScript engineer, I shove everything into JavaScript that I can."
- **CSS - just use Tailwind, it's awesome**
  - At paypal we had 90% unused CSS
- In Remix, when you don't want the CSS to apply, you remove it from the page
- Client-side server, state cache management and Nested Routing
  - Loaders run in parallel
  - Remix loads only what's needed
  - Mutations trigger invalidation of all loaders
  - Context for shared UI state and Remix for shared server state
  - No <Layout /> component

### The Point

- Trade-offs
  - Eliminate big problems in exchange for smaller ones
- Conclusion - Solving < Eliminating < Avoiding

kcd.im/problems-slides
