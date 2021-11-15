# Designing Reusable Components…That Are Actually Reusable

## Cory House

### Description

Modern UIs are often composed of reusable components written in React, Vue, Angular, whatever. In these modern technologies, creating a component is easy. However, creating a truly reusable component is hard. In this session, we'll explore the tradeoffs inherent in reusable component design, and discuss the questions to ask along the way. The examples presented will use React, but the concepts presented apply to anyone building components. After this session, you'll understand the key considerations required to create UI components that are truly reusable.

### Thoughts

- If you're working in any modern framework, then you are probably utilizing reusable components
- When it comes to reuse, I like to think about it as the hardest part of frontend development
  - As software developers we're really used to writing code that solves a problem. With a reusable component library you are writing code for people you haven't met for problems you haven't seen.
  - The benefit from utilizing reusable components is in being able to stand on the shoulders of giants (leveraging the time and effort that other developers spent to get reusability right)
- Balancing the good coding practices versus what my manager is expecting today
- If you want to have a component library that exists across multiple projects, then you need to pay someone a salary to build and maintain that library
- 7 developers on the team for the reusable library
  - by the time that Cory had left, they had shipped over 100 React apps
- Reusable components are not timeless, they reflect the current trends, and the current programmers on the team
- As society advances we take more things for granted
- Accessibility - utilizing the `for` parameter to make the app more accessible
- Using reusable components helps reduce decision fatigue
- Sometimes discussions on opinions on web technologies and languages can start to feel religious
- There's always going to be developers at your company that will be tempted to just code things on their own
- The documentation for the reusable components are extremely important!
  - storybook is the easy thing to do for docs
- If the demo isn't copy-pastable into my code, then that's a problem
- If you're building a component library right now, you should be using TypeScript
- It's helpful to group parent and child props together
- Usage - show people how to use the component with examples and props that make it happen
- Release notes - this way developers can see what/how you have changed (Breaking, Feature, Fix)
  - You want to minimize breaking releases
  - setting breaking releases to a certain timeframe means that the developers are dealing with pain longer
  - I don't think it's possible to programmatically generate really solid release notes
- People don't care about what you're fixing, they care about the behavior of the changes
- You do need to start with an audience of one, one project
  - Go pick a large ui component library that already exists as a starting point
    - Merely wrapping those open source projects
    - Removing settings, styling settings, and making it fit to your company needs
- Good developers are lazy - use other people's stuff wherever possible
- Audience: Project -> Team -> Business -> Public
- Balance programming consistency with leveraging flexibility
  - I like to start out very rigid
    - It's easy to add settings later, but it's challenging to remove settings
    - By starting out with a lean api, it's easier to implement, and it's less code
- The Tragedy of the Commons - Individuals behave contrary to the common good
- You need to have someone who is disagreeable on the Reusable component team, so they are comfortable with saying no to people that have requests
  - There has to be someone in control of the api, they have to have the big picture in their head, otherwise things will get more strung out and unrefined over time
- You can set props for your component api that will disable functionality within the component
  - TypeScript will set it to where you can programmatically enforce certain arguments into the component
- If you want people to use your components, give them the papercuts. Enforce the code practices that are expected.
- react doc gen - project to programmatically generate documentation - https://github.com/reactjs/react-docgen
  - wonderful way to set up documentation so you don't have to maintain two separate things
- how flexible should you be about styling?
  - even clients are internally torn about this
  - I could write my style in a way that is very open to extension
  - http://getbem.com/ - block element modifier - guidelines for styles
  - The rigid thing can go too far, because at a certain point the developer can choose to not use them
  - If they're done well, then they'll get adopted, otherwise they will be abandoned
- He will tweet out the slides afterwards
  - course on pluralsite to create reusable component libraries
