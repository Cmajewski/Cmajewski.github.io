---
layout: post
title:      "What type of React Component should you build? "
date:       2020-10-03 18:53:21 -0400
permalink:  what_type_of_react_component_should_you_build
---


When building React components, there are a number of ways to structure them and it’s important to understand the differences to correctly utilize these features.   

When should you use a functional component and when should you use a class component?

**Functional components**, sometimes referred to as stateless components, are plain Javascript functions that take in an argument of a prop and return a React element. You cannot call `this.state` inside a functional component.  You also cannot access lifecycle methods, such as `componentDidMount` in a functional component.  

**Class components** have a state and lifecycle methods, in addition to returning an element through the React render method. 

A general rule is that all presentational components that don’t need to hold a state should be functional components and all container components that hold logic should be component classes.  However, as many people experience, you may create a presentational functional component and then realize you want a counter button or a feature that requires a state after all.  Do you then need to change your functional component to a class component? This is where React 16.8 comes in and the introduction of React Hooks.

**React Hooks** are a new addition and allow you to use React features like state and lifecycle methods without using a class component.  

![](https://cdn1.bbcode0.com/uploads/2020/10/4/7f2667254a0d634040bee448b9b7bfad-full.png)

React Hooks are also regular Javascript functions with two main rules. 
* Don't use them inside loops, conditions or nested functions.
* Only use them from inside React functions.

There are 10 built in React Hooks and then you can write your own custom Hooks. The four most common ones are: 
1. useState()
2. useEffect()
3. useContext()
4. useReducer()

In the `useState()` Hook above you can see that it receives the first parameter `count` that is the current state of the counter.  The next parameter is `setCount` which is a method that will update the counters state, see below where it shows `setCount(count+1)` to increment the count.  The `useState()` hook receives an initial argument, which does not have to be an object, although it can be. The initial state is used only for the first render.  

React Hooks allow us to utilize functional components with the features of a class component, preventing unnecessary refactoring and making them stateful.  With the introduction of React hooks, now when do you use a functional component versus a class component?  The short answer is that it is now mostly preference.  Functional components have evolved in complexity with React Hooks and the official React documentation says the following. 

“We intend for Hooks to cover all existing use cases for classes, but we will keep supporting class components for the foreseeable future. At Facebook, we have tens of thousands of components written as classes, and we have absolutely no plans to rewrite them. Instead, we are starting to use Hooks in the new code side by side with classes.” — [React Docs](https://reactjs.org/docs/hooks-intro.html#gradual-adoption-strategy)


