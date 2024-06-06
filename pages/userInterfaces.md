# User Interfaces

<!--
These common user interface controls will render on any platform.
-->
---
transition: slide-left
---

## Button

<br>
<span>
A basic button component that should render nicely on any platform.
Supports a minimal level of customization.

</span>
<br>

```js
<Button
  onPress={onPressLearnMore}
  title="Learn More"
  color="#841584"
  accessibilityLabel="Learn more about this purple button"
/>
```

<br>

<br>
<span>
You can build your own button using<span v-mark.highlight.red="1"> Pressable </span>

</span>
<br>

```js
<Pressable onPress={onPressFunction}>
  <Text>I'm pressable!</Text>
</Pressable>
```

<br>

<!--
A basic button component that should render nicely on any platform
-->

---
transition: slide-left
---

## Switch

<br>
<span>
Renders a boolean input.

This is a controlled component that requires an `onValueChange` callback that updates the `value` prop in order for the component to reflect user actions.

</span>
<br>

```js
const SwitchDemo = () => {
  const [isEnabled, setIsEnabled] = useState(false);
  const toggleSwitch = () => setIsEnabled(previousState => !previousState);

  return (
    <Switch
        trackColor={{false: '#767577', true: '#81b0ff'}}
        thumbColor={isEnabled ? '#f5dd4b' : '#f4f3f4'}
        ios_backgroundColor="#3e3e3e"
        onValueChange={toggleSwitch}
        value={isEnabled}
    />
  );
};

export default SwitchDemo;
```

<br>

<!--
Renders a boolean input.
-->

---
transition: slide-left
---

# Flatlist

<br>
<span>
A performant interface for rendering basic, flat lists, supporting the most handy features:

- Fully cross-platform.
- Optional horizontal mode.
- Configurable viewability callbacks.
- Header support.
- Footer support.
- Separator support.
- Pull to Refresh.
- Scroll loading.
- ScrollToIndex support.
- Multiple column support.

</span>

<br>

> Shopify's Flashlist is a fast & performant list
<br>

<!--
Rendering basic, flat lists
-->
---
transition: slide-left
src: ./flexbox.md
---
