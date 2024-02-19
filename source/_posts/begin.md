---
title: 序言
tags:
  - meta
date: 2024/1/7
---

2024 年伊始，我的博客~~又双叒叕~~重启了一次

之前本来想用 Next.js 来写博客，但遇到了不少让我烦心的点：

1. MDX 虽然看起来很美好，但是其中间过一遍 rehype 转换成 HTML 再给 React 渲染的行为实际上损失了一些 Markdown AST 的信息（比如说，当你重写 MDX 的 `code` 组件时，你无法判断这是 mdast 中的 `InlineCode` 还是 `Code`）
2. Next.js 没有批量导入的支持（至少文档里没写，`require.context` 用起来略难受），Vite 的 `import.meta.glob` 至少可以手动标明类型，Astro Content Collections 就很不错
3. 使用 Server Component 集成 MathJax 的计划难产，MathJax 项目本身的 TypeScript 支持不太好，DOM Adaptor 的输出（一棵 DOM 树与一份全局 CSS）也并不适合 React（这方面 KaTeX 好一点，但 KaTeX 的渲染质量比 MathJax 差）（其实可以试试 MathML）

于是，最终我还是用回了 [Hexo](https://hexo.io/) + [NexT Theme](https://theme-next.js.org/) 的老组合，虽然之前一直在换架构导致博客中没有什么实际内容，不过后面就~~应该可能大概也许~~能保证会更新了🕊️
