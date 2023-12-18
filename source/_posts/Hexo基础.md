---
title: Hexo基础
date: 2023-09-12 21:09:51
tags: Hexo
---


# 常用命令
- `hexo new [layout] <title>`: 以指定布局（layout）和标题创建文章
- `hexo new page <title>`：在`source`目录下创建文件夹+index.md
- `hexo server`: 在本地运行项目
- `hexo generate`: 生成静态文件
- `hexo deploy`: 部署到远程站点

# 设置分类

- 创建分类：`hexo new page <category name>`在博客根目录下`source`文件夹中创建一个新的分类文件夹。
- 给文章设置分类：在文章的Front Matter中添加`categories`字段
  ```
  ---
  title: 我的技术文章
  date: 2023-09-20 14:00:00
  categories:
    - [category name]
  ---

  此文章属于xxx分类。
  ```
- 访问`http://your-blog-url/categories/<category name>/`可以查看该类目下所有文章

# 设置标签

在文章Front Matter中添加`tags`字段

```
---
title: 示例文章
date: 2023-09-19 10:00:00
tags:
  - 标签1
  - 标签2
  - 标签3
---
```

# 文章中引用本地图片


```
![图片描述](../img/posts/WX20231219-001924@2x.png)
```