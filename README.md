# qs-expand-flatten
[![NPM](https://nodei.co/npm/qs-expand-flatten.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/qs-expand-flatten/)
[![Build Status](https://travis-ci.org/marcosomma/qs-expand-flatten.svg?branch=master)](https://travis-ci.org/marcosomma/qs-expand-flatten)

Conversion functions between hash objects and objects.

## API

List of methods:

### expand(object)

**Arguments:**

  * `object` *Object* The hash object to expand.
  * `separator` *String* The digit used as separator

**Return value:** The expanded object.

**Syntax:**

```js
expand({ 'some.very.deep.prop': true }, '.');
// => result: { some: { very: { deep: { prop: true } } } }

expand({ 'some-very-deep-prop': true }, '-');
// => result: { some: { very: { deep: { prop: true } } } }
```

### flatten(object, check)

**Arguments:**

  * `object` *Object*   The object to flatten.
  * `check`  *Function* The checking handler (default: isNotObject).

**Return value:** The flattened hash object.

**Syntax:**

```js
flatten({ some: { very: { deep: { prop: true } } } });
// => result: { 'some.very.deep.prop': true }
```
