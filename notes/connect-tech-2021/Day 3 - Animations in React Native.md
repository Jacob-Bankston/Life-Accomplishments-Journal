# Animations in React Native

## Niya Panamdanam

### Description

This talk will walk through how to create animations in React Native, from practical user transitions to fun bouncy emojis. We will compare different animation tooling, their pros, and cons, to discover the best tool for the job.

### Thoughts

@findniya

- there is no dom
- there is no css
- react native has it's own language for movement
- performance
  - declarative vs imperative
    - declarative - gets the job done, you don't care about it
    - imperative - tells specifically how to get the job done
- what actually happens when you animate?
  - the animated api
  - JS animation driver uses requestAnimationFrame to execute on every frame
  - intermediate values are calculated and passed to View component
  - View is updated using setNativeProps
  - talks to the Native bridge
  - updates the UI Thread
  - A busy JS thread cause frame drops, frame drops are not a great user experience
    - It's trying to rerender the frame every 60 ms and it just can't keep up
- useNativeDriver
  - this moves all the JS thread steps to the Native Thread
  - Animated API produces a graph of animated nodes, which are all sent once to the Native Thread
  - Now the Native Thread can directly update the UI Thread and skip the JS Thread in between
- interpolation - interpolation is a type of estimation, a method of finding new data points based on the range of a discrete set of known data points
  - https://www.youtube.com/wwatch?v=ybcL8e6lmSo&ab_channel=eveningkid
- extrapolation & clamp
  - translation 0 to 100
  - opacity 0 to 1
  - Start to change opacity when translation = 25 and end when translation = 75
    - input range 25, 75 instead!
    - See pictures!
- Not everything that the Animated library can do is possible on the React Native
  - this where you leverage libraries to fill in what the animated api can not do
  - React Spring - a physics based animation library
    - It is built on Animated and React Motion
    - Brought in the abilities of Animated and added spring motion and declarative methods of React Motion
    - It works in web and mobile
  - Moti - built on reanimated v2 - abstracts the hooks to components that take an object
    - Combines the best of Framer Motion, React Spring and other libraries
    - Mobile/React Native first, but also works on other platforms
