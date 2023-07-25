# ScriptLoader

ScriptLoader is a lightweight and intuitive JavaScript utility designed to load scripts into your web pages. Developed as a modern successor to the much loved but no longer supported head.js, ScriptLoader retains the simplicity that developers have come to appreciate, while doing away with features no longer needed in modern web development.

## Background

Back in the day, we were regular users of head.js for its simplicity and ease of use. While other tools were complex and often loaded with features we didn't need, head.js stood out for being straightforward and doing one thing exceptionally well: loading scripts.

However, as time passed, head.js fell behind the curve due to lack of support and updates. Moreover, certain features that were critical in the days of head.js have become obsolete with advances in web development standards and practices.

As such, we decided to create ScriptLoader, a tool that carries forward the spirit of simplicity from head.js, but is updated to fit the requirements of modern web development. We've focused on features that matter most in today's context - parallel loading, ordered execution, and dependency management, and done away with the rest.

## Getting Started

Include the `ScriptLoader` script in your HTML file:

```html
<script src="path-to-script-loader.js"></script>
```

## Usage

```javascript
// Load scripts
ScriptLoader.load({
  'myscript1': 'https://path-to-your-script1.js',
  'myscript2': 'https://path-to-your-script2.js'
}, function() {
  console.log('All scripts loaded successfully!');
});

// Check if a script and its dependencies are ready
ScriptLoader.ready('myscript2', function() {
  console.log('myscript2 and all preceding scripts have loaded!');
  // You can put any additional code you want to execute here.
});
```

Replace path-to-script-loader.js with the actual path to the ScriptLoader script.

## Features
Parallel Loading: Enhance your page performance as all scripts are loaded in parallel.

Ordered Execution: Despite the parallel loading, scripts are executed in the order in which they were declared. This ensures the proper functioning of scripts that are dependent on others.

Dependency Management: With our 'ready' function, you can not only check if a script is ready, but also make sure all its dependencies (scripts declared before it) are ready.

## Limitations
While ScriptLoader is a simple tool for managing script loading, it doesn't provide advanced features found in full-featured module loaders or bundlers like RequireJS, SystemJS, or Webpack, such as:

Module support
Optimization and bundling
Transpilation
Source maps
Hot Module Replacement (HMR)
Code splitting and lazy loading
Plugins and loaders
Tree shaking
Please consider using a more sophisticated tool for substantial projects. ScriptLoader is best suited for small projects or learning purposes.

## Contributing
We welcome contributions from the community. If you wish to contribute, please fork the repository and submit a pull request.

