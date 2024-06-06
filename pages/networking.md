---
transition: slide-left
---

# Networking

<div>

React Native provides the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) for your networking needs. Networking is an inherently asynchronous operation.

```tsx
const getMoviesFromApi = () => {
  return fetch('https://reactnative.dev/movies.json')
    .then(response => response.json())
    .then(json => {
      return json.movies;
    })
    .catch(error => {
      console.error(error);
    });
};
```

</div>

<br>

> Third party libraries such as [axios](https://github.com/axios/axios) can be added and used instead.

<!--
`View`s are designed to be used with StyleSheet for clarity and performance, although inline styles are also supported.
-->

---
src: ./navigation.md
---
