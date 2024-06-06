# Layout with Flexbox

---
transition: slide-left
---

## What is flexbox

<br>
<div>
A component can specify the layout of its children using the Flexbox algorithm. Flexbox is designed to provide a consistent layout on different screen sizes.
</div>
<br>
<div>
We're primarily going to use a combination of <span v-mark.highlight.red="1"> flexDirection, </span> <span v-mark.highlight.red="2"> alignItems, </span> and <span v-mark.highlight.red="3"> justifyContent </span> to achieve the right layout.
</div>

<br>
<!--
This is to styling our components using flexbox to achieve responsiveness
-->


---
transition: slide-left
---

## Let's Flex 💪

<br>
<span>

`flex` will define how your items are going to `fill` over the available space along your main axis. Space will be divided according to each element's flex property.

</span>

```js
const FlexDemo = () => {
  return (
    <View
      style={{ flex: 1, padding: 20, flexDirection: "column", }}> // change 
      <View style={{ flex: 1, backgroundColor: "red" }} />
      <View style={{ flex: 2, backgroundColor: "orange" }} />
      <View style={{ flex: 3, backgroundColor: "green" }} />
    </View>
  );
};

export default FlexDemo;
```

<br>
<!--
A basic use of flex:
-->



---
transition: slide-left
---

# Flex Direction  ⬇️ ➡️ ⬆️ ⬅️ 

<br>
<span>

`flexDirection` controls the direction in which the children of a node are laid out. 

This is also referred to as the <span v-mark.box.orange="1"> main axis. </span>


- `column` <span v-mark.highlight.red="2"> (default value) </span> Aligns children from top to bottom.
- `row` Aligns children from left to right.
- `column-reverse` Aligns children from bottom to top.
- `row-reverse` Aligns children from right to left.

</span>
<br>
<br>
<br>

> Note: In web `flexDirection` defaults to column instead of row
> <br>

<!--
How flexDirection works:
-->


---
transition: slide-left
---

# Justify Content <carbon-text-align-justify />

<br>
<span>

`justifyContent` describes how to align children within the  <span v-mark.highlight.red="1"> main axis </span> of their container.


- `flex-start` (default value) 
- `flex-end`
- `center`
- `space-between` 
- `space-around` 
- `space-evenly` 

</span>
<br>

> Note: Compared to `space-between` using `space-around` will result in space being distributed to the beginning of the first child and end of the last child.
> <br>

<!-- 
- `flex-start (default value)` Align children of a container to the start of the container's main axis.
- `flex-end` Align children of a container to the end of the container's main axis.
- `center` Align children of a container in the center of the container's main axis.
- `space-between` Evenly space off children across the container's main axis, distributing the remaining space between the children.
- `space-around` Evenly space off children across the container's main axis, distributing the remaining space around the children. 
- `space-evenly` Evenly distribute children within the alignment container along the main axis.  -->




---
transition: slide-left
---

# Align Items 🙄

<br>
<span>

`alignItems` describes how to align children along the cross axis of their container.


- `stretch` (default value)  
- `flex-start`
- `flex-end`
- `center` 
- `baseline` 

</span>
<br>
<br>
<br>

> Info: For `stretch` to have an effect, children must not have a fixed dimension along the secondary axis

<!-- 
stretch (default value) Stretch children of a container to match the height of the container's cross axis.

flex-start Align children of a container to the start of the container's cross axis.

flex-end Align children of a container to the end of the container's cross axis.

center Align children of a container in the center of the container's cross axis.

baseline Align children of a container along a common baseline. Individual children can be set to be the reference baseline for their parents.
 -->


---
transition: slide-left
---

# Align Self 🧐

<br>

`alignSelf` has the same options and effect as alignItems but instead of affecting the children within a container, you can apply this property to a single child to change its alignment within its parent. It overrides 

<br>

> Info: For `stretch` to have an effect, children must not have a fixed dimension along the secondary axis
