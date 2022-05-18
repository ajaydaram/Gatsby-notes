# Create a page component
Gatsby contains two main components and one of them is page component and it cotains all the UI elements for the specific page
To create a page component Gatsby uses react 
For example let's create a page component for the Home component
If you are new for writing React concep there are three main steps involved
1. **Import** React from the 'react' package, so that you can use JSX inside your .js file.
2. **Define your component.** It should be a function that returns a JSX element.
3. **Export your component,** so that it can be used by other parts of your site.
Let us see with an example

```js
//Import React. This lets you use JSX inside your .js file.
import * as React from 'react'
/* Step 2: Define your component. Note that your
component name should start with a capital letter. */
  const AboutPage = () => {
   return(
   
         <h1> This is my info!</h1>
   
   )
      
  
  }

/* Step 3: Export your component so it
can be used by other parts of your app. */
export default AboutPage

```
**N0te** Always remeber that Your component must return a single React element, but you can put as many elements inside that top-level element as you want. The code snippet below shows an example of a valid component and an invalid component:

```js
import * as React from 'react'

const ValidComponent = () => {
  return (
    <div>
      <h1>A valid component!</h1>
      <p>This will work fine.</p>
      <p>
        Since there is only one top-level element: the div.
      </p>
    </div>
  )
}

const InvalidComponent = () => {
  return (
    <h1>This won't work.</h1>
    <p>Because there are two elements at the top level.</p>
  )
}
```
If you try to build your site with the code above, you’ll get an error for <InvalidComponent> like this:
  
  ```console
  Parsing error: Adjacent JSX elements must be
wrapped in an enclosing tag. Did you want a JSX fragment
<>...</>?  
 ```
