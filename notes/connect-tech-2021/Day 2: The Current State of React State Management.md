# The Current State of React State Management

## Riaz Virani

### Description

Trying to start a new React project and absolutely confused as to what state management library to use? Come learn how to make sense of the expansive set of options you have. We'll go over the history of React state management, what options you have today, and when you might want to choose one tool or the other.

### Thoughts

- There is not an official React state management solution
  - Why? We don't like standardization!
  - As a result, React's state management solutions have always been fragmented
- Other frameworks have taken a more cohesive approach
  - Ember (Ember Data), Angular (NgRx), Vue (VueX)
- React in comparison was only ever meant to design the view layer of the app
- React is explicitly not a MVC framework

### History

- React launches 2013
- Redux launches 2014
- Mobx launches 2015
- React Context launches 2018
- React Hooks launches 2019
- Atomic State is a thing 2020
- Query cache is a thing 2020
- UseSelectedContext starts 2021

There are many other options, but a majority of them were not adopted, and no longer used

### Redux

- Builds upon the Elm architecture
- Forces all state into a centralized store with known actions that can change state
- Forces each snapshot of changes to be immutable
- Forces you to write named types of changes to your state as actions
- View -> Actions -> State -> View...

- See picture of Redux Pros/Cons slide

- Opinion - It was great a the time as the est of the Flux inspired state management libraries. However, it's not necessarily the best developer experience available today. Hooks have dramatically reduced its reliance upon boilerplate.

### Mobx

- Redux has too much boilerplate, let's change to Mobx
- Built upon the concept of functional reactive programming
- Usually involves multiple stores in a single application whereas Redux usually has a single store
- Will be familiar to programmers coming from a functional programming background Moderately popular

- See picture of Mobx Pros/Cons slide

- Opinion - I don't like it but I have seen others that do really enjoy using it. I personally don't see the benefit over using an atomic state management library, which we will discuss later.

### React Context

- Put everything in Context

  - first option outside of component state built iinto React itself
  - Has a narrow focus in allowing components to share data without passing it via props, i.e. prop drilling
  - Intention was to store global data

- See picture of React Context Pros/Cons

- See picture for Opinion slide

### Hooks API

- See You've Got Me Hooked slide

- See picture of React Hooks Pros/Cons

- See picture of Opinion Time

### Atomic State Libraries

- Recoil is something that Facebook is building themselves
- Almost all of these libraries are built with suspense in mind

- See pictures

### Query Cache Libraries

- If you app is mostly just querying to grab data over and over, this could be a good solution for you
- **"Any time you get some magic you also get some mystery"**

- See pictures

### UseSelectedContext

- See pictures

### Theme

- Don't fit a square peg into a round hole. Use the tool that was designed for the job you're trying to accomplish.

riazv.me
@ViraniRiaz
