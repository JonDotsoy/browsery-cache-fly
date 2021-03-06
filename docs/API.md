# API

## CacheFly(optsArg, [transforms])

### Arguments

- **optsArg** *(Object|null)*: Options to cacheFly
- **[transforms]** *(...[Transform][Browserify Transform])*: Transform source code before parsing it for `require()` calls with the transform function or module name `tr`.

### Returns

- *(Array)*: Returns the transforms to browserify. With the validation of the files changed.

### Example
```javascript
const bundler = Browserify({
  transform: CacheFly(null, [Babelify, {preset: ["es2015"]}])
})
.bundle()
```

[Browserify Transform]: https://github.com/substack/module-deps#transforms
