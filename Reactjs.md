# ReactJs Introduction
1. General

ReactJs is frontend library

Every react application has at least one component which we refer to as the root component

The root component can contain child component (isolated and reuse)

It is essentially a tree of components

2. Component

Component is typically implemented as a Java script class that has some state and a render method


```javascript
class Tweet {
    state = {
        //Data
    };
    render () {
 
    }
}
```
- The output of render method is a react element which is a simple plain Js that maps to a Dom element
- It represents that Dom element in memory which were referred to as the Virtual Dom
- Unlike the real Dom, `this Virtual Dom is cheap to create`
- When we change the state of a component we get a new react element
- React will then compare this element and his children with the previous one, it figures out what is changed and then it will update a part of the real Dom to keep it in sync with the Virtual Dom
- Unlike vanilla js or jquery, we no longer have to work with the Dom API in browsers, in other words we no longer have to write code and query and manipulate the Dom or attach the event handlers to Dom elements, `we simply change the state of our components and react will automatically update the Dom to match that state`
- That's exactly why this library called react because `when the state changes react essentially reacts to state changes`

3. Compare Angular & React

| Table | Angular| React |
| ------| -------| ----- |
|Similar| Component based architecture
|Different|Is a framework or a complete solution| Is a library, it only takes care of rendering the view and making sure that the view is in sync with the state|

- So when building applications with react we need to use other libraries for things like routing or calling HTTP services...

# ReactJs Basic

## Install

```sh
npm i -g create-react-app@1.5.2
create-react-app react-app
```

It will create new application in name react-app with all the third-party libraries we need

- A lightweight development server
- Webpack from bundling our files
- Babel for compiling js code
- Other tools

## Basic command

`npm start` : Start the development server

`npm run build` : Bundles the app into static files for production

`npm test` : Starts the test runner

`npm run eject` : Removes this tool and copies build dependencies, configuration files and scripts into the app directory. If you do this, you can't go back!

## First application