---
id: 587d78a7367417b2b2512ae1
title: 使用 CSS 动画创建动画
challengeType: 0
videoUrl: 'https://scrimba.com/c/c7amZfW'
forumTopicId: 301051
---

# --description--

在元素的 `position` 已有指定值（如 `fixed` 或者 `relative`）时，CSS 偏移属性 `right`、`left`、`top`、`bottom` 可以用在动画规则里创建动作。

就像下面的例子展示的那样，你可以在 `50%` keyframe 处设置 `top` 属性为 50px，在开始（0%）和最后（100%）keyframe 处设置为 0px，以实现元素先向下运动，然后返回的动作效果。

```css
@keyframes rainbow {
  0% {
    background-color: blue;
    top: 0px;
  }
  50% {
    background-color: green;
    top: 50px;
  }
  100% {
    background-color: yellow;
    top: 0px;
  }
}
```

# --instructions--

请实现让 `div` 水平运动的效果。使用 `left` 偏移属性，添加 `@keyframes` 规则，让 rainbow 在 `0%` 的 `keyframe` 下从偏移 0 像素开始；在 `50%` 时偏移 25 像素；在 `100%` 时偏移 -25 像素。不要修改编辑器里的 `top` 属性，元素应该同时在水平和竖直方向运动。

# --hints--

`0%` 的 `@keyframes` 规则应为向 `left` 偏移 `0px`。

```js
assert(
  code.match(
    /0%\s*?{\s*?background-color:\s*?blue;\s*?top:\s*?0(px)?;\s*?left:\s*?0(px)?;\s*?}/gi
  )
);
```

`50%` 的 `@keyframes` 规则应为向 `left` 偏移 `25px`。

```js
assert(
  code.match(
    /50%\s*?{\s*?background-color:\s*?green;\s*?top:\s*?50px;\s*?left:\s*?25px;\s*?}/gi
  )
);
```

`100%` 的 `@keyframes` 规则应为向 `left` 偏移 `-25px`。

```js
assert(
  code.match(
    /100%\s*?{\s*?background-color:\s*?yellow;\s*?top:\s*?0(px)?;\s*?left:\s*?-25px;\s*?}/gi
  )
);
```

# --solutions--

