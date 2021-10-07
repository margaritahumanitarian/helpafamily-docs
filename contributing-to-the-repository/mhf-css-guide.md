# MHF CSS Guide

## CSS in JS

* **Avoid** the `inline style` attribute.

```javascript
// DO NOT DO THIS
<button className="btn" style={{margin: '10px'}} />
```

* **Avoid** `css modules` unless you are working on a whole page.

```javascript
// DO NOT DO THIS... most of the time
<button className={styles.btn} />
```

* **Use** the `styled jsx` library and follow [these conventions](https://nextjs.org/blog/styling-next-with-styled-jsx).

```javascript
// CORRECT!
<button className="btn" />
<style jsx>{`.btn {...}`}</style>
```

### Styled JSX

**Styled JSX** is a small library built into Next.js. It's built and maintained by Vercel and therefor integrates nicely. There's a small learning curve to using it. Here are some basics.

#### Using the library

Implementing a styled jsx element is simple. You simply insert **this block**:

```text
<style jsx>{``}</style>
```

into your **React Component** in your return area, like so.

```javascript
const MyComponent = () => {
    return (
    <div>
        <input />
        <buton />
        <style jsx>{``}</style>
    </div>
}
```

You don't have to import the library, you can just use it out of the box.

{% hint style="info" %}
Note the **back ticks**. Styled JSX uses something called template strings. Similar to what you would see in a GraphQL call if you've ever used that. So similarly, there's a handy [VScode extension](https://marketplace.visualstudio.com/items?itemName=blanu.vscode-styled-jsx) to help see your CSS in the style JSX block with color and linting enabled. 
{% endhint %}

### Writing CSS

So now we can simply insert class names and in the **styled JSX** element we write our CSS the way we would in any CSS file. Again, the [VScode extension](https://marketplace.visualstudio.com/items?itemName=blanu.vscode-styled-jsx) does wonders here and I would highly recommend you use it.

```javascript
const MyComponent = () => {
    return (
    <div className="my-wrapper">
        <input className="my-input" />
        <buton className="my-btn" />
        <style jsx>{`
            .my-wrapper {
                height: 100vh;
            }
            .my-input {
                padding: 10px;
            }
            .my-btn {
                background: salmon;
            }
        `}</style>
    </div>
}
```

### Scoping CSS

Styled JSX is scoped, so you can be more free with your class naming, just make sure it stays scoped in the case of sub components or a wrapper component.

```javascript
<div id="container">
  <div className="my-class">
    // MyComponent is considered scoped to this container
    <MyComponent />
  </div>

  <styled jsx>`
  .my-class {
    height: 100vh;
  }
  `</styled>
</div>
```

