---
transition: slide-left
layout: center
---
# Debugging

React Native provides an in-app developer menu which offers several debugging options. You can access the Dev Menu by shaking your device or via keyboard shortcuts:

- iOS Simulator: <kbd>Cmd ⌘</kbd> + <kbd>D</kbd> (or Device > Shake)
- Android emulators: <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (macOS) or <kbd>Ctrl</kbd> + <kbd>M</kbd> (Windows and Linux)

Alternatively for Android devices and emulators, you can run `adb shell input keyevent 82` in your terminal.

<span v-mark.highlight.red="1">Reactotron</span> can monitor application's state, network requests, and performance metrics.

<br>

> npx react-devtools

<br>

> npx react-native start --experimental-debugger

or press <kbd>J</kbd>

<!--
Debugging Basics
-->

---
transition: slide-left
---

# Recommendation

- Avoid *UI re-renders*
  - UI flickering
  - Frames dropping
- Make use of `Typescript` for writing code and `Storybook` for documentations.
- Use dedicated Components like flashList, fast-image etc
- Always animate at 60 FPS
- Create pure components while dividing your components into presentation and container components while keeping your UI and business logic separate.

<!--
Debugging Basics
-->

---
transition: slide-left
---

# Expo

<br>
<div>
<span>Expo is a production-grade React Native <span v-mark.highlight.red="1">Framework.</span> Expo provides developer tooling that makes developing apps easier, such as file-based routing, a standard library of native modules, and much more.</span>
<br>
<br>
<span>Expo's Framework is free and open source, with an active community on <a href="https://github.com/expo">GitHub</a> and <a href="https://chat.expo.dev">Discord</a>. The Expo team works in close collaboration with the React Native team at Meta to bring the latest React Native features to the Expo SDK.</span>
<br>
<br>
<span>The team at Expo also provides <span v-mark.underline.yellow="2">Expo Application Services (EAS)</span>, an optional set of services that complements Expo, the Framework, in each step of the development process.</span>
<br>
<br>
</div>

<!--
RN components equivalent Android vs iOS vs Web
-->

---
src: ./nativeModules.md
---
