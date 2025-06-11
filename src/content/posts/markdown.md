---
title: "markdown语法"
columns: ["工具"]
published: "2024-09-06 01:00:00"
---

## 1. Markdown 基础语法

### 1.1. 标题

**语法：**

```markdown
# This is an h1 title

## This is an h2 title

### This is an h3 title

#### This is an h4 title
```

**实例：**

# This is an h1 title

## This is an h2 title

### This is an h3 title

#### This is an h4 title

### 1.2. 强调和斜体

**语法：**

```markdown
_This text will be italic_

**This text will be bold**
```

**实例：**

_This text will be italic_

**This will also be bold**

### 1.3. 有序列表和无序列表

**语法：**

```markdown
- Item 1
- Item 2
- Item 3

1. Item 1
2. Item 2
3. Item 3
```

**实例：**

- Item 1
- Item 2
- Item 3

1. Item 1
2. Item 2
3. Item 3

### 1.4. 图片

**语法：**

```markdown
![img-name](img-url)
```

**实例：**
![一只熊](https://placebear.com/200/300)

### 1.5. 超链接

**语法：**

```markdown
[link-name](link-url)
```

**实例：**

[冴羽](https://juejin.cn/user/712139234359182/posts)

### 1.6. 引用

**语法：**

```markdown
> xxxx
```

**实例：**

> 君子有九思：视思明，听思聪，色思温，貌思恭，言思忠，事思敬，疑思问，忿思难，见得思义

### 1.7. 单行代码

**语法：**

```markdown
`This is an inline code.`
```

**实例：**

`This is an inline code.`

### 1.8. 多行代码

**语法：**

````
​```javascript
for (var i = 0; i < 100; i++) {
    console.log("hello world");
}
​```
````

**实例：**

```js
for (var i = 0; i < 100; i++) {
  console.log("hello world");
}
```

## 2. GFM

### 2.1. 自动链接语法

**语法：**

```
www.example.com
```

**实例：**

www.example.com

### 2.2. 脚注

**语法：**

```
A note[^1]

[^1]: Big note.
```

**实例：**

A note[^1]

[^1]: Big note.

### 2.3. 删除线

**语法：**

```
~one~ or ~~two~~ tildes.
```

**实例：**

~one~ or ~~two~~ tildes.

### 2.4. 表格

**语法：**

```
| a   | b   |   c |  d  |
| --- | :-- | --: | :-: |
```

**实例：**

| a   | b   |   c |  d  |
| --- | :-- | --: | :-: |

### 2.5. 任务列表

**语法：**

```
- [ ] to do
- [x] done
```

**实例：**

- [ ] to do
- [x] done

## 3. SmartyPants（转印刷体）

### 3.1. 直引号（ " 和 ' ）转弯引号

**语法：**

```
"SmartyPants" 和 'SmartyPants'
```

**实例：**

"SmartyPants" 和 'SmartyPants'

### 3.2. 反引号转弯引号

**语法：**

```
``like this''
```

**实例：**

``like this''

### 3.3. `--` 转 en-dash，`---` 转 em-dash

**语法：**

```
1962--1968

A penny saved is a penny earned. —--Benjamin Franklin
```

**实例：**

1962--1968

A penny saved is a penny earned. —--Benjamin Franklin

### 3.4. 三个连续的点转省略号

**语法：**

```
...
```

**实例：**

...

## 4. 插件

### 4.1. emojis 添加可访问性（rehype-accessible-emojis）

愿你开心每一天！😁

### 4.2. 颜色可视化（rehype-color-chips）

The background color is `#ffffff` for light mode and `#000000` for dark mode.

### 4.3. GitHub Alert 语法

**语法：**

```
> [!NOTE] 注意
> The custom title will replace the regular title.

> [!TIP] 技巧
> Helpful advice for doing things better or more easily.

> [!IMPORTANT] 重要
> Key information users need to know to achieve their goal.

> [!WARNING] 警告
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION] 谨慎
> Advises about risks or negative outcomes of certain actions.
```

**实例：**

> [!NOTE] 注意
> The custom title will replace the regular title.

> [!TIP] 技巧
> Helpful advice for doing things better or more easily.

> [!IMPORTANT] 重要
> Key information users need to know to achieve their goal.

> [!WARNING] 警告
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION] 谨慎
> Advises about risks or negative outcomes of certain actions.

### 4.4. 数学表达式

**The Cauchy-Schwarz Inequality**

$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

## 5. 自定义插件

### 5.1. GitHub Card

**语法：**

```
::github{repo="mqyqingfeng/blog"}
```

**实例：**

::github{repo="mqyqingfeng/blog"}
