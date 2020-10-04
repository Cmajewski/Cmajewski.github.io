---
layout: post
title:      "When to use React State versus Redux Store"
date:       2020-10-04 00:25:13 -0400
permalink:  when_to_use_react_state_versus_redux_store
---


Organizing state in components can be complicated and begs the question, should all stateful components be connected to the Redux store. While the Redux store can be a very powerful tool, no this is not always the case. Sometimes it makes sense to store the state locally in the React component.  

*When do you use React state and when do you use the Redux Store? *

The Redux store should be used when unrelated components need to access the same state. Passing state through many parent and child components will get very messy and the store quickly fixes this problem.  Additionally, the Redux Store is a great solution when you are keeping track of any state changes. 

![](https://i.imgur.com/1C1vjMd.png)

The React local state should be used when the state is only relevant to the component you are in or when state doesn’t need to be persisted when the component is unmounted. 

**Pros of Redux Store**
* Stored locally 
* Central store and easy to access
* Prevents unnecessary re-renders
* Better for debugging


**Pros of React Local State**
* Ideal for simple state or when UI changes occur
* Preferable for small projects

The official Redux page notes in many cases it is up to the developer. 


![](https://imgur.com/ge7ZNby.png)

