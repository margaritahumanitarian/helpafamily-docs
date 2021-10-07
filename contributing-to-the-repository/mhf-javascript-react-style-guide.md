# MHF Javascript/React Style Guide

## React Components

### Favor arrow functions for components

```javascript
const MyComponent = () => {
  ...
}
```

> Using arrow functions avoids the `this` keyword behavior nuances

### Destructure Props

```javascript
(props) should be ({propName1, propName2})
```

> This gives clarity to the codebase in your components use of props

### Exports

Favor `export default` for components and make one component per file as opposed to `named export` with multiple components.

```javascript
const MyComponent = () => {
  ...
}

export default MyComponent
```

> Though Typescript recommends this practice for code readability, there is no hard reasoning for this rule except for consistency.

If your component seems better suited with named exports feel free to do so.

**Note: Utility and Constants Files**

`named exports` are better for these files.

```javascript
export function myHelper(){
  ...
}
```

### Component Naming

Use the filename as the component name.

```javascript
const MyComponent = () => {...}
// should be 
MyComponent.js
```

### Props Naming

Avoid using DOM component prop names for anything except the DOM attribute.

Wrong:

```javascript
<MyComponent onClick={handleClick} />
...
const MyComponent = ({onClick}) => {
  ...
  setIsEditing(!onClick)
  ...
}
```

Correct:

```javascript
<MyComponent isEditing={handleIsEditing} />
...
const MyComponent = ({isEditing}) => {
  ...
  setIsEditing(!isEditing)
  ...
}
```

Correct use of a DOM attribute

```javascript
<MyComponent onClick={handleClick} />
...
const MyComponent = ({onClick}) => {
  return <button onClick={onClick}>
}
```

### JSDOC

Use JsDoc to document your component and its props. This isn't mandatory, but it does help a lot. 

```javascript
/**
* MyComponent does x, y, z
*
* @param {Object} props - { propOne }
* @param {String} props.propOne - propOne does x, y, z
*
*/
const MyComponent = ({propOne}) => {...}
```



