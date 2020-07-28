## Chrome DevTools and Web Runtime Performance

###### Chrome DevTools
- A set of web developer tools build directly into the Google Chrome browser

- Help to edit pages on the fly and diagnose problems quickly


Open dev tools: `Command + Option + I`
Goto the console panel directly: `Command + Option + J`

** (On Windows: `Control + Shift` instead of `Command + Option`)

###### Discover DevTools

`Command + Shift + P`:
    
   - Change the placement (bottom/right)
   - Show coverage
   - Rendering
   - Capture screenshot(node/capture area/full-size )
   - many more…

`Command + Shift + O` (on a file) – will show all methods in the file

###### Console Log
We can get our log in a nice way using dev tools. Here are some examples:

```js
const animals = [
   { name: 'cat', color: 'white’ },
    { name: 'dog', color: 'black' },
    { name: 'zebra', color: 'black and white stripes' }
];

console.log(animals);
console.log({animals});
console.table(animals);
console.table(animals, ['name']);

 animals.forEach(animal => {
    console.groupCollapsed(`${animal.name}`);
    console.log(`This is ${animal.name}`);
    console.log(`${animal.name} color is ${animal.color}`);
    console.groupEnd(`${animal.name}`);
});

console.count('Count');

console.log('%c This is a colorful text with red background! ', 'background: #f00; color: #bada55');
```

We can run a demo now. Open the `console-log.html` file in the browser and see the output in the console.

For the coverage-test, we check the unused bytes for the page by running the `index` page in the browser. Guide has been written in the page to generate the coverage report.


Next: [Web Runtime Performance](./WEB_RUNTIME_PERF.md)

