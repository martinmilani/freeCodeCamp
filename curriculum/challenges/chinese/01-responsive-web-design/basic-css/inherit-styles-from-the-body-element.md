---
id: bad87fee1348bd9aedf08746
title: 从 body 元素继承样式
challengeType: 0
videoUrl: 'https://scrimba.com/c/c9bmdtR'
forumTopicId: 18204
---

# --description--

我们已经证明每一个 HTML 页面都含有 `body` 元素，我们也可以在 `body` 元素上使用 CSS 样式。

设置 `body` 元素样式的方法跟设置其他 HTML 元素样式的方式一样，并且其他元素也会继承 `body` 中所设置的样式。

# --instructions--

首先，创建一个内容文本为 `Hello World` 的 `h1` 元素。

接着，在 `body` 的 CSS 规则里面添加 `color: green;`，这会将页面内所有字体的颜色都设置为绿色。

最后，在 `body` 的 CSS 规则里面添加 `font-family: monospace;`，这会将页面内所有字体的 `font-family` 都设置为 `monospace`。

# --hints--

应创建一个 `h1` 元素。

```js
assert($('h1').length > 0);
```

`h1` 元素的内容文本应为 `Hello World`。

```js
assert(
  $('h1').length > 0 &&
    $('h1')
      .text()
      .match(/hello world/i)
);
```

确保 `h1` 元素具有结束标签。

```js
assert(
  code.match(/<\/h1>/g) &&
    code.match(/<h1/g) &&
    code.match(/<\/h1>/g).length === code.match(/<h1/g).length
);
```

`body` 元素的 `color` 属性值应为 `green`。

```js
assert($('body').css('color') === 'rgb(0, 128, 0)');
```

`body` 元素的 `font-family` 属性值应为 `monospace`。

```js
assert(
  $('body')
    .css('font-family')
    .match(/monospace/i)
);
```

`h1` 元素应该继承 `body` 的 `monospace` 字体属性。

```js
assert(
  $('h1').length > 0 &&
    $('h1')
      .css('font-family')
      .match(/monospace/i)
);
```

`h1` 元素的字体颜色应继承 `body` 元素所设置的绿色。

```js
assert($('h1').length > 0 && $('h1').css('color') === 'rgb(0, 128, 0)');
```

# --solutions--

