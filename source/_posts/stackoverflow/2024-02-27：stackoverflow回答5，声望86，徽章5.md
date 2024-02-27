---
title: 2024-02-27：stackoverflow回答5，声望86，徽章5
date: 2024-02-27 22:29:54
tags: stackoverflow
categories:
  - stackoverflow
---

## 2024-02-27：更新声望


- 回答：+2到达5
- 声望：+25到达86
- 徽章：+1达到5


# 第5个回答

题目:[How do I remove the blue square that appears when I click the button on small screens?](https://stackoverflow.com/a/78068129/22510112)

题主想去掉手机浏览器中点击button的时候显示一个表示选中状态的背景颜色。使用[-webkit-tap-highlight-color](https://developer.mozilla.org/en-US/docs/Web/CSS/-webkit-tap-highlight-color)即可。

答案：

```
button {
  -webkit-tap-highlight-color: transparent;
}
```
