---
layout: post
title:      "What type of React Component should you build? "
date:       2020-10-03 22:53:20 +0000
permalink:  what_type_of_react_component_should_you_build
---


When building React components, there are a number of ways to structure them and it’s important to understand the differences to correctly utilize their different features.   

The first is when should you use a functional component and when should you use a class component?

**Functional components**, sometimes referred to as stateless components, are plain Javascript functions that take in an argument of a prop and return a React element. You cannot call `this.state` inside a functional component.  You also cannot access lifecycle methods, such as `componentDidMount` in a functional component.  

**Class components** have a state and lifecycle methods and return an element through the React render method. 

A general rule is that all presentational components that don’t need to hold a state should be functional components and all container components that hold logic should be component classes.  However, as many people experience, you may create a presentational functional component and then realize you want a counter button or a feature that requires a state after you build it.  Do you then change your functional component to a class component? This is where React 16.8 and the introduction of React Hooks comes into play. 

**React Hooks** are a new addition and allow you to use React features like state and lifecycle methods without using a class component.  

[](https://im6.ezgif.com/tmp/ezgif-6-05b094d9f9cc.png)

React Hooks allow us to utilize functional components with the features of a class component, preventing unnecessary refactoring and making them stateful.  With the introduction of React hooks, now when do you use a functional component versus a class component?  The short answer is that it is now mostly preference.  Functional components have evolved in complexity with React Hooks and the official React documentation says the following. 

“We intend for Hooks to cover all existing use cases for classes, but we will keep supporting class components for the foreseeable future. At Facebook, we have tens of thousands of components written as classes, and we have absolutely no plans to rewrite them. Instead, we are starting to use Hooks in the new code side by side with classes.” — [React Docs](https://reactjs.org/docs/hooks-intro.html#gradual-adoption-strategy)

