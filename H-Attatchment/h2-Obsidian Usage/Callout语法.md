callout 是 obsidian 的特有语法，源于 markdown 的引用语法`>` 。

## 语法

### 基本语法

```
> [!NOTE] Title
> Content
```

NOTE可换为以下：
1. note
2. abstract, summary, tldr
3. info
4. todo
5. tip, hint, important
6. success, check, done
7. question, help, faq
8. warning, caution, attention
9. failure, fail, missing
10. danger, error
11. bug
12. example
13. quote, cite

### 展开与折叠

```
> [!NOTE]+ 左边多了个加号
> 代表 Callout 默认展开

> [!NOTE]- 左边多了个减号
> 代表 Callout 默认折叠
```

> [!NOTE]+ 左边多了个加号
> 代表 Callout 默认展开

> [!NOTE]- 左边多了个减号
> 代表 Callout 默认折叠

### 嵌套使用

```
> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.
```

> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.

