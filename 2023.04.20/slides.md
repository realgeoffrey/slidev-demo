---
# try also 'default' to start simple
theme: seriph
# titleTemplate for the webpage, `%s` will be replaced by the page's title
titleTemplate: '%s'
# information for your slides, can be a markdown string
info: 2023.04.20小组分享

# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://cn.sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: true
# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: slide-left
# use UnoCSS
css: unocss
---




# Typescript的奇技淫巧

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
    <a href="https://github.com/realgeoffrey/knowledge/blob/master/网站前端/Typescript学习笔记/README.md" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />realgeoffrey
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://cn.sli.dev/guide/syntax.html#notes)
-->








---
transition: fade-out
---
# What is Typescript?

<br>

<v-clicks>

- 是JS的一个超集，主要提供了类型系统和对ES6的支持。

- TS的类型系统被设计为可选的，因此，JS就是TS。

- TS不会阻止JS的运行，即使存在类型错误也不例外，这能让JS逐步迁移至TS。

- ... 略
</v-clicks>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
本人是入职K歌之后才使用TS。

一开始看了几篇ts的电子书，然后在工作中边学边用，从硬着头皮写、到处都是 `any` ，再到现在尽量不用`any`。

不过现在想用ts实现一些**有想法**的类型去约束的时候，却还是找不到方法。
-->










---
transition: fade-out
---
# 我对TS的个人看法

<br>

<v-clicks>

1. 直接写JS而不用TS，会难受。
2. 用了TS，感觉花了时间琢磨类型，但是代码大部分又是自己看自己改，写不写类型代码一样跑。

    >尤其是刚写React的.tsx时。
3. 看别人写的TS，又没有比看JS好到哪里去，该难受的还是难受。

    - 可能：可读性和可维护性，重要的不是类型声明，重要的还是代码结构和编程习惯。
4. TS收益：除了降低维护成本，可能更重要的是保持团队在类型约束环境下的开发状态，养成类型思维。
</v-clicks>

<!--

-->







---
transition: fade-out
---
# Typescript 重点、难点

|     |     |
| --- | --- |
| 类（class）| 在TS里既是类型，也是函数（构造函数）。<br>相对于函数，使用 类 可以省去给函数声明类型。 |
| 泛型（Generics） | 1. 泛型函数、接口、类型别名、类 <br> 2. 泛型约束 |
| 内置类型别名 | `Partial`、`Record`、`Pick`、等（[typescript: Utility Types](https://www.typescriptlang.org/docs/handbook/utility-types.html)） |
| 一些关键字 | `typeof`、`keyof`、`in`、`infer`、等 |
| 协变与逆变 | <p v-click><MdiHeadQuestionOutline/><MdiHeadQuestionOutline/><MdiHeadQuestionOutline/></p> |
| ... | ... |





---
src: ./pages/index.md
---



---
transition: fade-out
---

## 在项目中使用 自定义`泛型`、处理`协变与逆变`的问题

<v-clicks>

...略

</v-clicks>

<!--
比较复杂，就不说了……
-->






---
transition: fade-out
layout: cover
class: text-center
background: './public/1.jpg'
---
# Learn More

[<carbon-logo-github />type-fest](https://github.com/sindresorhus/type-fest) · [<carbon-logo-github />typescript-exercises](https://github.com/typescript-exercises/typescript-exercises) · [<carbon-logo-github />react-redux-typescript-guide](https://github.com/piotrwitek/react-redux-typescript-guide)
