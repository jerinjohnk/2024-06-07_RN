# Hooks

<!--
These common user interface controls will render on any platform.
-->
---
transition: slide-left
---

<br>
<div>
<span>React Hooks provide<span v-mark.highlight.yellow="1"> functional components </span> with the ability to use states and manage side effects.</span>
<span> They were first introduced in <span v-mark.circle.pink="2">React 16.8 </span>. They provide a cleaner and more concise way to handle state and side effects in React applications. </span>
<br>
<br>
</div>


<br>
<span>
Hook Rules
There are 3 rules for hooks:

- Hooks can only be called inside React function components.
- Hooks can only be called at the top level of a component.
- Hooks cannot be conditional

</span>

<br>

---
transition: slide-left
---

# useState

<span>`useState` is a React Hook that lets you add a<span v-mark.highlight.pink="1"> state variable </span> to your component.</span>
<br>
```shell
const [state, setState] = useState(initialState)
```

Call useState at the top level of your component to declare one or more state variables.
<br>

```js
import { useState } from 'react';

function MyComponent() {
  const [count, setCount] = useState(0);
  //...
}

```
<br>
<div>
<span>The convention is to name state variables like<span v-mark.box.yellow="2"> `[something,setSomething]` using array destructuring.</span> </span>

<span>useState returns an array with exactly two items</span>

<span>- The <span  v-mark.highlight.blue="3"> current state </span>of this state variable, initially set to the <span  v-mark.highlight.purple="4"> initial state </span> you provided.</span>

<span>- The <span  v-mark.highlight.yellow="5"> set function </span>  that lets you change it to any other value in response to interaction.
</span>
</div>



---
transition: slide-left
---

# useEffect

React useEffect hook handles the effects of the dependency array. The useEffect Hook allows us to perform side effects on the components. fetching data, directly updating the DOM and timers are some side effects. It is called every time any state if the dependency array is modified or updated
<br>
```shell
useEffect(<FUNCTION>, RETURN , [DEPENDENCY])
```
<br>
React useEffect Hook ShortHand for:

- FUNCTION: contains the code to be executed when useEffect triggers.

- RETURN: runs one final time after your component is removed (unmounts).

- DEPENDENCY: is an optional parameter, useEffect triggers when the given dependency is changed.

---
transition: slide-left
---

# Example of useEffect

```js

import React, { useState, useEffect } from 'react'
import { Button } from 'react-native'

export default function App() {
  const [count, setCount] = useState(0)

  useEffect(() => {
    console.log(count)
  }, [count])

  return (
    <Button
      title={`Increment ${count}`}
      onPress={() => {
        setCount(count + 1)
        //  setCount(prevState => prevState + 1) ) //ascynch 
      }}
    />
  )
}

```

---
transition: slide-left
---

# useRef

useRef is a React Hook that lets you reference a value that’s not needed for rendering.
<br>

```shell
const ref = useRef(initialValue)
```
<br>

# useCallback

useCallback is a React Hook that lets you cache a function definition between re-renders.
<br>

```shell
const cachedFn = useCallback(fn, dependencies)
```
<br>

# useMemo

useMemo is a React Hook that lets you cache the result of a calculation between re-renders.
<br>

```shell
const cachedValue = useMemo(calculateValue, dependencies)
```
<br>


---
transition: slide-left
---

<!-- # useReducer

useReducer is a React Hook that lets you add a reducer to your component.
<br>

```shell
const [state, dispatch] = useReducer(reducer, initialArg, init?)
```
<br>

# useContext

useContext is a React Hook that lets you read and subscribe to context from your component.
<br>

```shell
const value = useContext(SomeContext)
```
</br> -->
