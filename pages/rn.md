# What is React Native?

<br>
<div class="grid grid-cols-2 gap-8">
  <div>
  <span>React Native is an open source framework for building Android and iOS applications using React and the app platform’s native capabilities.</span>
  <br>
  <br>
  <span>With React Native, you use<span v-mark.highlight.red="1"> JavaScript </span>to access your <span v-mark.underline.orange="2">platform’s APIs</span> as well as to describe the appearance and behavior of your <span v-mark.underline.orange="3">UI</span> using React components: bundles of reusable, nestable code.
  </span>
  </div>
  <div>
  <img src="/diagram_react-native-components_dark.svg" width="400" alt="A diagram showing React Native's Core Components are a subset of React Components that ship with React Native." />
 </div>
</div>

<!--
RN components equivalent Android vs iOS vs Web
-->

---
transition: slide-left
---

## Expo

<br>
<div>
<span>Expo is a production-grade React Native<span v-mark.highlight.yellow="1"> Framework </span>. Expo provides developer tooling that makes developing apps easier, such as file-based routing, a standard library of native modules, and much more.</span>
<br>
<br>
<span>Expo's Framework is free and open source, with an active community on <a href="https://github.com/expo">GitHub</a> and <a href="https://chat.expo.dev">Discord</a>. The Expo team works in close collaboration with the React Native team at Meta to bring the latest React Native features to the Expo SDK.</span>
<br>
<br>
<span>The team at Expo also provides<span v-mark.circle.blue="2"> Expo Application Services (EAS), </span>an optional set of services that complements Expo, the Framework, in each step of the development process.</span>
<br>
<br>
</div>

<!--
RN components equivalent Android vs iOS vs Web
-->

---
transition: slide-left
---
# Get Started Without a Framework

<https://reactnative.dev/docs/getting-started-without-a-framework>

<br>
```shell
npx @react-native-community/cli@latest init rnWorkshop
```
<br>
<div v-click="1">
```shell
Need to install the following packages:
@react-native-community/cli@13.6.6
Ok to proceed? (y) y
```
</div>

<br>
<div v-click="2">
```shell
✔ Installing dependencies
✔ Do you want to install CocoaPods now? Only needed if you run your project in Xcode directly … (y) y
```
</div>

<br>
<div v-click="3">
```shell
Run instructions for iOS:
    • cd "/Users/jerin/rn/demo/rnWorkshop"
    • npx react-native run-ios
    or
    • npx react-native run-android
```
</div>

<!--
Getting started
-->

---
transition: slide-left
layout: image-left
image: /folder.png
---

## Folder structure and keywords
<br>

### JSX

React and React Native use **JSX,** a syntax that lets you write elements inside JavaScript like so: `<Text>Hello, I am your cat!</Text>`.

### Props

**Props** is short for “properties”. Props let you customize React components.

### State

**State** is useful for handling data that changes over time or that comes from user interaction. State gives your components memory!

<!--
RN components equivalent Android vs iOS vs Web
-->

---
transition: slide-left
---

## Views and mobile development

In Android and iOS development, a **view** is the basic building block of UI: a small rectangular element on the screen which can be used to display text, images, or respond to user input. Even the smallest visual elements of an app, like a line of text or a button, are kinds of views. Some kinds of views can contain other views. It’s views all the way down!

<div class="flex justify-center items-center">
<figure>
  <img src="/diagram_ios-android-views.svg" width="400" alt="Diagram of Android and iOS app showing them both built on top of atomic elements called views." />
</figure>
</div>

<!--
RN components equivalent Android vs iOS vs Web
-->

---
transition: slide-left
---

## Core Components

<br>

| React Native UI Component | Android View   | iOS View         | Web Analog              | Description                                                                                           |
| ------------------------- | -------------- | ---------------- | ----------------------- | ----------------------------------------------------------------------------------------------------- |
| `<View>`                  | `<ViewGroup>`  | `<UIView>`       | A non-scrolling `<div>` | A container that supports layout with flexbox, style, some touch handling, and accessibility controls |
| `<Text>`                  | `<TextView>`   | `<UITextView>`   | `<p>`                   | Displays, styles, and nests strings of text and even handles touch events                             |
| `<Image>`                 | `<ImageView>`  | `<UIImageView>`  | `<img>`                 | Displays different types of images                                                                    |
| `<ScrollView>`            | `<ScrollView>` | `<UIScrollView>` | `<div>`                 | A generic scrolling container that can contain multiple components and views                          |
| `<TextInput>`             | `<EditText>`   | `<UITextField>`  | `<input type="text">`   | Allows the user to enter text                                                                         |

<style>
tr {
  font-size: 14px
}
</style>

<!--
RN components equivalent Android vs iOS vs Web
-->

---
transition: slide-left
---

<div grid="~ cols-5">
<div class="col-span-1">

<img src="/Demo1.png" width="400" alt="Demo1" />

</div>
<div class="col-span-4" >

````md magic-move {lines: true}
```js {2|4-7|9}
// step 1 Define Component
import React from 'react';

function Demo1() {
  return (
  );
}

export default Demo1;
```

```js {7|3}
// step 2 Adding Text
import React from 'react';
import { Text } from 'react-native';

function Demo1() {
  return (
    <Text>Demo1</Text>
  );
}

export default Demo1;
```

```js {8-13|3}
// step 3 Adding Image
import React from 'react';
import { Text, Image } from 'react-native';

function Demo1() {
  return (
    <Text>Demo1</Text>
    <Image
      source={{
        uri: 'https://ddragon.leagueoflegends.com/cdn/9.1.1/img/profileicon/588.png',
      }}
      style={{ width: 100, height: 100 }}
    />
  );
}

export default Demo1;
```

```js {7,15|3}
// step 4 Fix:- JSX expressions must have one parent element
import React from 'react';
import { Text, Image, View } from 'react-native';

function Demo1() {
  return (
    <View style={{ backgroundColor: '#FF0' }}>
      <Text>Demo1</Text>
      <Image
        source={{
          uri: 'https://ddragon.leagueoflegends.com/cdn/9.1.1/img/profileicon/588.png',
        }}
        style={{ width: 100, height: 100 }}
      />
    </View>
  );
}

export default Demo1;
```

```js {7,17|3}
// step 4 Fix:- JSX expressions must have one parent element
import React from 'react';
import { Text, Image, View, SafeAreaView } from 'react-native';

function Demo1() {
  return (
    <SafeAreaView>
     <View style={{ backgroundColor: '#FF0' }}>
        <Text>Demo1</Text>
        <Image
          source={{
            uri: 'https://ddragon.leagueoflegends.com/cdn/9.1.1/img/profileicon/588.png',
          }}
          style={{ width: 100, height: 100 }}
        />
      </View>
    </SafeAreaView>
  );
}

export default Demo1;
```

```js {21,29|22-24|8|25-28|14|*}
// step 5 Fix:- Inline styling
import React from 'react';
import {Text, Image, View, SafeAreaView, StyleSheet} from 'react-native';

function Demo1() {
  return (
    <SafeAreaView>
      <View style={styles.container}>
        <Text>Demo1</Text>
        <Image
          source={{
            uri: 'https://ddragon.leagueoflegends.com/cdn/9.1.1/img/profileicon/588.png',
          }}
          style={styles.image}
        />
      </View>
    </SafeAreaView>
  );
}

const styles = StyleSheet.create({
  container: {
    backgroundColor: '#FF0',
  },
  image: {
    width: 100,
    height: 100,
  },
});

export default Demo1;
```
````

</div>
</div>
<!--
Here is another comment.
-->

---
transition: slide-left
src: ./components.md
layout: center
---
