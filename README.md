# tenoxui-classes-converter
Function to generate tenoxui's classes.

## Usage

This is basic usage :
```js
const inputClasses = {
  center: {
    display: "flex",
    alignItems: "center",
    justifyContent: "center"
  },
};

const transformedClasses = transformClasses(inputClasses);
console.log(transformedClasses);
```

Output :

```js
{
  display: { center: 'flex' },
  alignItems: { center: 'center' },
  justifyContent: { center: 'center' }
}
```

Or, use with tenoxui :

```js
new makeTenoxUI({
  element: /*...*/,
  classes: transformClasses({
    "my-box": {
      "--color": "red",
      backgroundColor: "var(--color)",
      padding: "1rem"
    },
    center: {
      display: "flex",
      alignItems: "center",
      justifyContent: "center"
    }
  })
});
```
