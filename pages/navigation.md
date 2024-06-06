---
transition: slide-left
---

# Navigating Between Screens

<div>

React Navigation is used for managing the presentation of, and transition between, multiple screens which is typically handled a navigator.
<br>

```shell
npm install @react-navigation/native @react-navigation/native-stack
npm install react-native-screens react-native-safe-area-context
```

<br>

```tsx
import {NavigationContainer} from '@react-navigation/native';

const App = () => {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen
          name="Home"
          component={HomeScreen}
          options={{title: 'Welcome'}}
        />
        <Stack.Screen name="Profile" component={ProfileScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
};

```

</div>
<br>

<!--
Navigating between screens part 1
-->

---
transition: slide-up
hideInToc: true
---

<div>

- You can set options such as the screen title for each screen in the `options` prop of `Stack.Screen`.
- Each screen takes a `component` prop that is a React component.
- Those components receive a prop called `navigation` which has various methods to link to other screens. For example, you can use `navigation.navigate` to go to the `Profile` screen:

<br>

</div>

```tsx
const HomeScreen = ({navigation}) => {
  return (
    <Button
      title="Go to Jane's profile"
      onPress={() =>
        navigation.navigate('Profile', {name: 'Jane'})
      }
    />
  );
};
const ProfileScreen = ({navigation, route}) => {
  return <Text>This is {route.params.name}'s profile</Text>;
};

```

<br>

<!--
Navigating between screens part2
-->

---
src: ./animations.md
---
