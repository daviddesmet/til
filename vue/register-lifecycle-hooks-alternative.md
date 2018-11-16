# Alternative way to register lifecycle hooks

```javascript
mounted() {
  const scrollHandler = () => {
    ...
  };

  window.addEventListener("scroll", scrollHandler);
  // listen to the hook destroy event and run once
  this.$once("hook:destroyed", () => {
    window.removeEventListener("scroll", scrollHandler);
  });
}
```