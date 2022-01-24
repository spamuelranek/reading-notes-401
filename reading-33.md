# Nextjs and React

## [Nextjs](https://nextjs.org/learn/basics/create-nextjs-app)
- Framework for react
  - needs to be budled and transformed
  - productino optimizations
  - pre-render pages for performance and SEO
  - connect app to data stores

- Next.js is a framework
  - page-based routing system
  - pre-rendering
  - automic code splitting
  - client-side routing
  - built-in CSS
  - Fast Refresh support

- Navigate Between Pages
 - based around the `<Link>` tage when it is wrapped around `<a>`
 - ` import Link from 'next/link'`
 - `<Link>` takes an href in a path structure off of the base url or directory 
 - Next.js spits the code automatically
  - only the page you are visiting will be loading
  - but it also pre-fetches the pages that are present in any of the links you have on your page.

- Assets, Metadata, and CSS
 - `<Image>` tag from `'next/image'`
 - `<Head>` tag from `'next/head'`

## [React Context for Beginners](https://www.freecodecamp.org/news/react-context-for-beginners/)

### React Context?
- React context allows us to pass down and consume data in whatever component we need withour using props
- Examples when it makes sense
  - User Data
  - Location-specific Data

- Data that does not have to be updated
  - context was not for complete state management

- What does it solve?
  -  Simplifies Props drilling
  - This is done by wrapping a components or multiple components in a `UserContext.Provider` tag and wrapping the children components in a `UserContext.Consumer` tag

``` javascript
import React from 'react';

export const UserContext = React.createContext();

export default function App() {
  return (
    <UserContext.Provider value="Reed">
      <User />
    </UserContext.Provider>
  )
}

function User() {
  return (
    <UserContext.Consumer>
      {value => <h1>{value}</h1>} 
      {/* prints: Reed */}
    </UserContext.Consumer>
  )
}
```
- attr: [freeCodeCamp React Context By: Reed Barger](https://www.freecodecamp.org/news/react-context-for-beginners/)

 - Another form is:
  - `useContext` hook
    - create a variable = `React.createContext()
    - The parent component acts the same
      - the child can then just create a variable of `React.useContext(UserContext)` to access the data

  - Thinking Reactly:
    - Dont always look to `useContext` sometimes there is a better way to pass the props in an container or structure

  - This is not a state management system
    - updates things will not cause re-renders on things from contextProvider

[ Return to Home](README.md)