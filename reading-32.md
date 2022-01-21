# Back at it in React

## [React Conditional from Docs](https://reactjs.org/docs/conditional-rendering.html)
- functional components
  - can return an element
  - encapulate the conditional inside another component
  - pass the changing variable in as props

- keys and list
  - work as it does in JS
  - with the added benefit of being able to return JSX

- forms
  - how the terrible end users interact with us

```html
<form>
  <label> Hello Lame-o 
    <input type= "text" name = "losers_name">
  </label>
  <input type = "submit" value ="How lame are you">
```

- Composition vs Inheritance
  -  `props.children`
    - allows for arbitrar amount of children in that space

- Thinking in React
  - Start with a mock up
  - Break the UI into a component Hierarchy

  - Build a static version of the page
  - Identify the minimal Representation of UI state
    - what will need to talk to what
    - what will be collecting data
  - Where your state should live
    - what will be conditional on that data
    - what are children of other things
    - where does the state need to be shared