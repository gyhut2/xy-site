---
icon: lucide/rocket
---

# 开始使用
如需完整文档，请访问 [zensical.org](https://zensical.org/docs/).

## 命令

* [`zensical new`][new] - 创建一个新项目
* [`zensical serve`][serve] - 启动本地Web服务器
* [`zensical build`][build] - 构建你的网站

  [new]: https://zensical.org/docs/usage/new/
  [serve]: https://zensical.org/docs/usage/preview/
  [build]: https://zensical.org/docs/usage/build/

## 示例

## 提示信息

> 转到 [文档](https://zensical.org/docs/authoring/admonitions/)

!!! note

    这是一个**注释**警告。用于提供有用的信息。

!!! warning

    这是一个**警告**提示。请小心！

### 详情

> 转到 [文档](https://zensical.org/docs/authoring/admonitions/#collapsible-blocks)

??? info "点击展开了解更多信息"

    此内容在您点击展开前是隐藏的。
    非常适合用于常见问题解答或长篇解释。

## 代码块

> 转到 [文档](https://zensical.org/docs/authoring/code-blocks/)

``` python hl_lines="2" title="Code blocks"
def greet(name):
    print(f"Hello, {name}!") # (1)!

greet("Python")
```

1.  > 转到 [文档](https://zensical.org/docs/authoring/code-blocks/#code-annotations)

    代码注释允许将备注附加到代码行上。

代码也可以在内联中高亮显示: `#!python print("Hello, Python!")`.

## 内容标签

> 转到 [文档](https://zensical.org/docs/authoring/content-tabs/)

=== "Python"

    ``` python
    print("Hello from Python!")
    ```

=== "Rust"

    ``` rs
    println!("Hello from Rust!");
    ```

## 图表

> 转到 [文档](https://zensical.org/docs/authoring/diagrams/)

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

## 脚注

> 转到 [文档](https://zensical.org/docs/authoring/footnotes/)

这是一个带有脚注的句子。[^1]
悬停它，以查看提示信息。
[^1]:这是脚注。


## 格式化

> 转到 [文档](https://zensical.org/docs/authoring/formatting/)

- ==这被标记了（高亮）==
- ^^这是插入的（下划线）^^
- ~~这条内容已被删除（删除线）~~
- H~2~O
- A^T^A
- ++ctrl+alt+del++

## 图标、表情符号

> 转到 [文档](https://zensical.org/docs/authoring/icons-emojis/)

* :sparkles: `:sparkles:`
* :rocket: `:rocket:`
* :tada: `:tada:`
* :memo: `:memo:`
* :eyes: `:eyes:`

## 数学公式

> 转到 [文档](https://zensical.org/docs/authoring/math/)

$$
\cos x=\sum_{k=0}^{\infty}\frac{(-1)^k}{(2k)!}x^{2k}
$$

！警告“需要配置”
请注意，MathJax是在本页上通过一个｀script`标签集成的，且未在生成
的默认配置中进行配置，以避免将其包含在不需要此功能的页面中。如需
详细了解如何在所有页面（如果其数学内容比这些简单的起始页面更为丰
富）上进行配置的相关细节，请参阅相关文档。

<script id="MathJax-script" src="https://unpkg.com/mathjax@3/es5/tex-mml-chtml.js"></script>
<script>
  window.MathJax = {
    tex: {
      inlineMath: [["\\(", "\\)"]],
      displayMath: [["\\[", "\\]"]],
      processEscapes: true,
      processEnvironments: true
    },
    options: {
      ignoreHtmlClass: ".*|",
      processHtmlClass: "arithmatex"
    }
  };

  document$.subscribe(() => {
    MathJax.startup.output.clearCache()
    MathJax.typesetClear()
    MathJax.texReset()
    MathJax.typesetPromise()
  })
</script>

## 任务列表

> 转到 [文档](https://zensical.org/docs/authoring/lists/#using-task-lists)

* [x] 安装Zensica
* [x] 配置`zensical.toml
* [x] 撰写出色的文档
* [ ] 部署到任何地方

## 工具提示

> 转到 [文档](https://zensical.org/docs/authoring/tooltips/)

[悬停我][example]

  [example]:https://example.com "我是提示框！"
