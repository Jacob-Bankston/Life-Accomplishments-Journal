# Super Simple Start to Remix

## Kent C. Dodds

### Description

Remix has me more excited about building better websites than anything else since I started using React back in 2015. I have so much to say about it, but for this blog post, we're going to remove as many distractions as possible and give remix the "super simple start" treatment. So, even though Remix has a fancy npm init remix thing you can run (which is much easier than what I'm going to show you), we're going to skip that and build a simple remix app from absolutely nothing to running so we can inspect each bit required to get it going.

### Thoughts

- The purpose of this talk is supposed to be the most bare bones simplistic set up for a Remix application

- Not going to cover everything you can do with Remix
- Not going to directly compare to other frameworks

- Remix will set up a generator and bake in all of the files for you

- When you're first learning something you should set up everything yourself to understand where the lines are drawn for everything

### Remix

- Up until recently it was a paid software
  - They are going open source
  - They still haven't moved everything over to open source just yet
- add a `.npmrc` file
- install dependencies!
  - react, react-dom, react-router-dom
- install dev depencies
  - @remix-run/dev
- When you're starting something new, get it to a deployable state
  - If you're just playing around, who cares about CI/CD
- Joke: Error driven development - Coding via the error messages
- need the remix.config.js file in the directory
- need the entry.client.jsx file in the directory
- need the entry.server.jsx file in the directory
- need the root.jsx file in the directory
- Server
  - build folder
    - assets.json
    - index.js
- public/build
  - Served as a static file
- In jsx you render your HTML element within the Remix framework
- You get to be the one that gets to load `ReactDOM.hydrate(<RemixBrowser />, document)`
- install remix
- Can host and deploy Remix in a bunch of different places, within a docker container, all cloud platforms, etc...
- `install @remix-run/react @remix-run/serve`
- `npx remix setup node`
- **Go is very fast! Using esbuild under the hood**
  - Learn Go lang!
- The build and watch mode are writing files to disk because it's just so fast... Less than a second usually.
- You are in control on whether there is any JavaScript loading on this page in Remix
  - The questions of how to handle things within Remix ultimately are structured by the web apis
- package build, public and dependencies, throw it in a docker container and ship it out there

- https://remix.run/

  - website for React Remix

- icanhasdadjoke.com
  - dad joke generator
  - "You know how jokes are funnier when you explain them?"

https://esbuild.github.io/

- esbuild's website

- Nested routing, the rest of the app still works!

  - File based routing, it was the conventions that are used anyway, and now it is programmatically enforced/supported?

- will be posting the code onto github - https://github.com/kentcdodds
