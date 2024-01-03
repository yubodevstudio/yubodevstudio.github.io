---
title: '2024-01-03：stackoverflow回答3，声望61，徽章4'
date: 2024-01-03 21:44:30
tags: stackoverflow
categories:
  - stackoverflow
---

# 2024-01-03：更新声望

- 回答+2
- 声望+25


# 第2个回答

题目:[My CSS is my react app isn't working as expected](https://stackoverflow.com/q/77731089/22510112)

题目如下：
> I'm working in this code branch. It's a simple contacts app written with React as a self-study exercise.
>
> My current problem is that when I click my add contact button, the add contact form in my modal is not styled correctly.
> I'm trying to style it to modal-content from ./css/addContactModal.module.css which is called within AddContactModal.js. enter image description here Can someone advise me where I've gone wrong with respect to changing the modal form's CSS?
>

题主css文件中的class名字使用了`-`，在jsx中没有正确使用类名导致无法正确使用样式，这里我没细看题目理解错了以为整个样式没加载，还是要加强审题，没有被采纳，得到一个vote up，声望+10

> i have downloaded your code and it works well. your code is correct and style is appled to the correct element.
>
> you can add below css to addContactModal.module.css
> ```
> .modal input {
>   background-color: red;
> }
> ```

# 第3个回答

题目：[Getting content overlapped while having fixed navbar](https://stackoverflow.com/q/77749582/22510112)

题目如下：

> I am trying to have a top text and navbar fixed at the top of the page and it should not scroll up with the content. I was able to fix it at the top by using position:fixed,but content is getting overlapped.
>
> I used position: position:sticky, set margin and padding, but nothing helped.
>
> I want to know how neatly I can achieve this. Please help

题主想实现一个顶部导航fixed，效果但是内容被导航遮挡了。给内容设置一个顶部空白空间给导航栏即可，答案被采纳，声望+15

> add padding top to your content:
> ```
> #content {
>  padding-top: 80px; /* height of your nav */
> }
> ```