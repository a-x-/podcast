# #1 pilot episode shownotes

- [Итак, вы хотите научиться функциональному программированию (серия статей)](https://medium.com/devschacht/charles-scalfani-so-you-want-to-be-a-functional-programmer-part-1-6ef98e90d58d)
- [Введение в Immutable.js и основные концепции функционального программирования](https://medium.com/devschacht/sebastián-peyrott-introduction-to-immutablejs-and-functional-programming-concepts-b3a6555af0ee)
- Haskell: функции, типы, классы типов (как интерфейсы)
- [eax.me/monads](http://eax.me/monads/)
- [ruhaskell.org](https://ruhaskell.org)
- [ohaskell.guide](https://ohaskell.guide/init.html)
- Maybe monad
- promise
- [immutable-js get default](https://twitter.com/mxtnr/status/907543174666706944)
- Either monad
- [ramda Either](https://github.com/ramda/ramda-fantasy/blob/master/docs/Either.md)
- [null bad](https://www.lucidchart.com/techblog/2015/08/31/the-worst-mistake-of-computer-science/) — есть хорошая таблица с десятками языками и их null и maybe эквивалинтах
- [maybe at npm](https://www.npmjs.com/package/maybe)
- [ramda at npm](https://www.npmjs.com/package/ramda)
- null — reject — optional chaining
- смешивание reject и throw и уровни ошибок
- [Default parameters @ MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)
- богатство системы типов: множества как в математике

**Figure 1.** falsy checks
```js
v == null // то же самое что v === undefined || v === null

// https://lodash.com/docs/#isNil
_.isNil(value) // Checks if value is null or undefined
_.isNull(value) // Checks if value is null

!v // any falsy value, e.g. 0, '', false, null, undefined
```

**Figure 2.** default args
```js
const f = (a = 1) => a

f() // 1
f(undefined) // 1
f(null) // null
```

**Figure 3.** old bad defaults
```js
function (a) {
  a = a || 1 // Ugly bad, causes deoptimization
}
```

**Figure 4.** [immutable-js](https://github.com/facebook/immutable-js) `get(path, default)`
```js
get('key', 42)
get('key') || 42
maybe(get('key'), 42) // stupid lazy maybe = (val, def) => val == null ? val : def
```
----

Спасибо Вове [@tempname11](https://github.com/tempname11) за ответы на вопросы.

> Дьявол является начальником церкви, он является начальником секты дьявола. ~ [@neural_machine](https://twitter.com/neural_machine/status/962839388437778434)
