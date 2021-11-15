# Brick by Brick: What Lego Taught Me About Great APIs

## Ray Gesualdo

### Description

It had been over a decade since I put together a Lego set. But a recent gift changed everything and I quickly found myself captivated building a new Lego model. As I went, I realized so many of the wonderful things that make Lego amazing apply beyond the boundaries of plastic brick building. They apply directly to APIs! Join me as we delve into the Lego building experience and the lessons we can learn along the way to make our APIs Lego-level great.

### Thoughts

- "Nothing happens if you don't tweet about it"
- I enjoyed it so much that I thought "there's a conference talk in here somewhere." What did Lego do so well that made the experience so gratifying
- Been doing web-dev for 7 years, and web-adjacent for 16 years
  - @raygesualdo
  - full-stack but focused on front-end lately
  - worked on a variety of projects
  - Salesloft
- A majority of our code is typically used by all of our other developers on a daily basis, so there is a lot of responsibility there when constructing the APIs

### APIs

- Broaden your definition of APIs from just Web APIs to any place that data will pass between two locations
- customer - the person who is going to be using what we built
  - paying customer
  - coworker across from you
  - you in 6 months
- Think of your API as a product

### 5 Things to Think About - Comparing Lego to an API

1. Documentation
   1. Lego
      1. Clear
      2. Step by Step
      3. Physical and Digital documentation
   2. API
      1. Clarity
         1. Much of the Open Source documentation will be written from the author's perspective, but it lacks in clarity from a new "customer's" perspective
      2. Being able to step through the documentation
         1. Including all of the information on how to handle each aspect in the documentation with all pertinent information without skipping any steps (no matter how small)
      3. Multi-Modal documentation
         1. Having the extensive documentation in addition to having the inline documentation as needed
         2. Do you have the ability to try out the different types of the code
         3. This can describe any way that your customers can interact with your documentation
      4. Is it clear, is it well written, is it multi-modal, are the customers able to use it whatever level they are at?
      5. Are the customers able to get to the information that they need quickly? (Compare to being able to Google the serial number of pieces or the number of the set)
   3. The purpose of documentation is about lowering the barrier of entry to allow customers to be able to utilize your api
2. Compose-ability
   1. Lego
      1. NPU - Nice Parts Usage - Reusability!
      2. They built up a system where the pieces could be used and designed and used in many different ways
   2. API
      1. As we are providing support and tooling for the customer we need to be intentional about what ways the customer can utilize all the tooling
3. Consistency
   1. Lego
      1. Every single piece of Lego follows the same specifications and measurements that are rigorously and routinely followed.
   2. API
      1. Reducing guesswork for our customers
         1. Naming conventions need to be absolutely consistent - should not have redundant terminology (fetch, get, grab, etc...)
            1. "The human brain wants to follow a pattern match"
            2. Can someone use 2 or 3 of the things in your API and reliably guess how the rest of the things work?
4. Compatibility
   1. Lego
      1. Backwards Compatibility - Standard Lego Brick started in 1959 and could be used in a set today
   2. API
      1. We want to make sure that we do not have any unnecessary or frequent breaking changes
      2. Allows the customers to be able to pattern match with what we are building
      3. Not cause pain, but accelerate what they're trying to do
      4. How do we make sure what code the customers are already using doesn't break
5. Empathy
   1. Lego
      1. When you have a product, you want to empathize with the customer and give them something that they wanted to be provided
      2. Whatever nerdom you're a part of there's a lego set/community for that
   2. API
      1. As we're building and developing our product, are we thinking about the human being on the other side
