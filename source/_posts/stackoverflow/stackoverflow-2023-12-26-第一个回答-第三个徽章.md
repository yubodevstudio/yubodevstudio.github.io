---
title: 'stackoverflow 2023-12-26: 第一个回答+第三个徽章'
date: 2023-12-26 00:47:10
tags: stackoverflow
categories:
  - stackoverflow
---


# 第一个回答

题目:[Div that expands only upwards and scrolls at max height](https://stackoverflow.com/q/77712519/22510112)

题目如下：

> So I'm writing a frontend with react and I have a chat window that looks like so
>
>  <div id="outer-wrapper">
>    <div className = "chat-window-wrapper">
>      <div className="chat-window">
>        <!-- chat messages go here -->
>        </div>
>        <div className="chat-window-textarea"></div>
>      </div>
>
>      <div id="element-below">
>          <!-- other stuff -->
>      </div>
>  </div>
>inside of the chat-window div I am using react to render messages from an observable array of messages, each message inside of chat-window looks like this:
>
>    <div>
>        {messageStr}
>    </div>
>I calculate the height of the chat-window-wrapper div based on the amount of messages in react and it works great, and I have a max height that the outer div can expand to that works great. I'm working on getting the inside of chat-window-wrapper to look right
>
>I need the chat-window-textarea to remain anchored to the bottom, currently it sits kind of in the middle of the messages with a lot of empty space below it
>I need chat-window-wrapper to only expand upwards, currently if I hit the max height the window starts to expand downwards and the element-below gets pushed off the screen. I want chat-window to scroll if chat-window-wrapper reaches max height
>I'm collaborating on a larger project, so I'm currently treating outer-wrapper and element-below as a black box, but I can change the css on those elements if absolutely necessary
>
>How would I go about doing this with css? I have tried a bunch of stuff, and I can post my janky css files if needed, but I think I'm going to have to start from scratch anyway. Any guidance is appreciated even if it's just a small suggestion
>
>Thanks

题主大概是要实现一个聊天APP界面，消息从底部向上显示，底部有一个操作区域。使用flex布局即可。回答如下：

> it seems that you are working on a chat app which show messages from new to old and have a textarea to edit message.  for your question:
>
> 1. make `chat-window-textarea` to the bottom: you can use flex layout in the  parent element `chat-widnow-wrapper` and set `flex-direction: column`, set chat-window to take the rest space;
> 2. make `chat-window-wrapper` to expand upwards: use flex and flex-direction: column-reverse;
>
> the css is below:
>
> ```
>   .chat-window-wrapper {
>     width: 100px; /* for demo */
>     border: 1px solid #eaeaea; /* for demo */
>     height: 100px;
>     display: flex;
>     flex-direction: column; /* Reverse column to make it expand upwards */
>   }
>
>   .chat-window {
>     display: flex;
>     flex-direction: column-reverse;
>     overflow-y: auto; /* Enable vertical scroll if needed */
>     flex: 1;
>   }
> ```
>
> demo: https://codepen.io/nxoglrnh-the-decoder/pen/eYXmWYW


大概意思是通过
1. 使用`flex-direction: column;`设置聊天记录和操作区上下分布，聊天记录`flex: 1;`占据全部剩余空间，确保操作区在底部
2. 聊天记录`flex-direction: column-reverse;`实现从下向上滚动显示聊天记录。

编辑答案意外获得<a href="https://stackoverflow.com/help/badges/3/editor?userid=22510112" target="_blank" class="so-badge so-badge-bronze">Editor</a>徽章