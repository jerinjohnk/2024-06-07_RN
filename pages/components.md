# Basic Components

<!--
Most apps will end up using one or more of these basic components.
-->
---
transition: slide-left
---

## View

`View` is a container that supports layout with flexbox, style, some touch handling, and accessibility controls.

```js
import React from 'react';
import {View, Text} from 'react-native';

const ViewDemo = () => {
  return (
    <View
      style={{
        flexDirection: 'row',
        height: 100,
      }}>
      <View style={{backgroundColor: 'blue', flex: 0.3}} />
      <View style={{backgroundColor: 'red', flex: 0.5}} />
      <Text>Hello World!</Text>
    </View>
  );
};

export default ViewDemo;
```

>`View` is designed to be nested inside other views and can have 0 to many children of any type.

<!--
`View`s are designed to be used with StyleSheet for clarity and performance, although inline styles are also supported.
-->

---
transition: slide-left
---

## Text

A React component for displaying text. `Text` supports nesting, styling, and touch handling.

```js
import React from 'react';
import {Text, StyleSheet} from 'react-native';

const TextDemo = () => {
  const titleText = "Bird's Nest";

  return <Text style={styles.titleText}>{titleText}</Text>;
};

const styles = StyleSheet.create({
  titleText: {
    fontSize: 20,
    fontWeight: 'bold',
  },
});

export default TextDemo;
```

<br>

<!--
Nested text, Container
-->

---
transition: slide-left
---

## Image

A React component for displaying different types of images, including network images, static resources, temporary local images, and images from local disk, such as the camera roll.

```js
import React from 'react';
import {Image, StyleSheet} from 'react-native';

const ImageDemo = () => (
  <Image
    style={styles.tinyLogo}
    source={{
      uri: 'https://reactnative.dev/img/tiny_logo.png',
    }}
  />
);

const styles = StyleSheet.create({
  tinyLogo: {
    width: 50,
    height: 50,
  },
});

export default ImageDemo;
```

<br>

<!--
For network and data images, you will need to manually specify the dimensions of your image!
-->

---
transition: slide-left
---

## TextInput

Component for inputting text via a keyboard. Props provide configurability for several features, such as auto-correction, auto-capitalization, placeholder text, and different keyboard types, such as a numeric keypad.

You can also subscribe to the `onChangeText`, `onSubmitEditing` and `onFocus` events to read the user input.

```js
import React from 'react';
import {StyleSheet, TextInput} from 'react-native';

export const TextInputDemo = () => {
  const [text, onChangeText] = React.useState('Useless Text');

  return (
    <TextInput style={styles.input} onChangeText={onChangeText} value={text} />
  );
};

const styles = StyleSheet.create({
  input: {
    height: 40,
  },
});
```

<br>

<!--
For network and data images, you will need to manually specify the dimensions of your image!
-->

---
transition: slide-left
---

## ScrollView

`ScrollViews` must have a bounded height in order to work, since they contain unbounded-height children into a bounded container

```js
const ScrollViewDemo = () => {
  return (
    <ScrollView
      style={styles.container}
      contentContainerStyle={styles.scrollContent}>
      <Text>Lorem ipsum dolor sit</Text>
    </ScrollView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
  },
  scrollContent: {
    backgroundColor: 'pink',
    marginHorizontal: 20,
  }
});

export default ScrollViewDemo;
```

<br>

<!--
For network and data images, you will need to manually specify the dimensions of your image!
-->
