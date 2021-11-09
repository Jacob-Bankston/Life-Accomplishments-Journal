# Build Fullstack Apps in Record Time with Blitz.js

## Brandon Bayer

### Description

Blitz.js is the Fullstack React Framework. It's heavily inspired by Ruby on Rails and is focused on making you as productive as possible. It extends Next.js and adds all the missing pieces you need for building a fullstack app with a database. By far the biggest innovation of Blitz is the new "Zero-API" data layer that abstracts away the API so you don't have to mess with REST or GraphQL APIs! And out of the box so many things are already set up like ESLint, Jest, and even a production ready user authentication and authorization system! Brandon will cover all that and provide you everything you need to start using Blitz yourself.

### Thoughts

- Creator of Blitz to construct fullstack apps
- Anything that got in the way of me building features slowly got in the way of my morale
- Two things I had to have, "Monolithic" and "No API"
- Started out with the architecture being SSR, but didn't love it. What would this look like if it was easy?

### Blitz - what is has in it

- Next.js is really cool because it is a flexible hybrid framework
  - You can build a fullstack app just with Next.js
- Blitz is a fork of Next.js that adds power features for building fullstack apps
  - We merge and continue to maintain compatibility from Next.js

### Prisma loaded into the feature stack as well

- Next-generation Node.js and TypeScript ORM
- Handles everything you need on the database side
- fully typed based on your database schema (much simpler flow compared to sequelize, it looks like)

### Foundational Principles

- Fullstack and Monolithic
- API Not Required
- Convention over Configuration
- Loose Opinions
- Easy to Start, Easy to Scale
- Stability (After 1.0)
- Community over Code

### Menial Setup Done For You

- All the boring stuff is done for you out of the box
- Folder structure
- ESLint
- Prettier
- Husky
- Jest
- Database
- Forms
- User sign-up, log-in, logout (never have to do authentication again)
- Reset password flow

### "Zero-API" Data Layer

- We abstract the API into a compile step
- Write code that runs on server and import directly into your frontend
- Don't have to mess with REST or GraphQL APIs
- Enabled via Blitz queries and mutations

### Live Demo

`blitz new`

- TypeScript is highly recommended
- We're not trying to optimize for minimal files and downloads, we are trying to integrate all of the files that you will most likely need as a default boilerplate as possible.
- We set up a sequel-lite database by default
- Login, Sign Up, Reset Password all baked in to the startup template
- integrated all of the set up structural things with their cli to integrate the prisma side of things for the CRUD operations
- integration with zod package -> sets standards for typing across your api
- authentication and authorization are enabled by default
- Handles the Date serializations, Maps, Regex, etc... for you
- has React Suspense built in
- prisma studio is a localhost display of all the tables within your database - great ui visualization
  - https://www.prisma.io/react-server-components
- https://blitzjs.com/
- Blitz Recipes
  - 1 command to install arbiitrary third-party code
  - Perfect for libraries requiring setup
- Ruby on Rails equivalent with Blitz Console

### Other Features

- Passport.js adapter for social login
- HTTP Middleware
- Advanced data serialization
- Deploy to a server or serverless
- Custom server
- Database agnostic

### Current Status

- Late beta/nearing release candidate
- 1.0 expected before end of year
- 10,000 Github stars
- 2,300 members in Discord

blitzjs.com/fame

### Try blitz in Under 5 Minutes

1. `yarn global add blitz`
2. `blitz new myApp`

### Contributing - Open Source Project

- We need your help!
- You can become involved as much as you want, become maintainer, etc...

### Flight Control

flightcontrol.dev

- optimizing for blitz and next
- will bbe adding serverless
- eventually expand to other services and languages

### Get Started

blitzjs.com
@flybayer & @blitz_js
blitzjs.com/stickers - Free Stickers (will send you free stickers anywhere in the world)
