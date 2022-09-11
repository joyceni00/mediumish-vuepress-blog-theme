---
title: What's the most beautiful website in the world
date: 2020-1-28
tags:
- frontmatter
- vuepress
author: John Doe
featuredimg: https://images.unsplash.com/photo-1568777036071-f9a769596a49?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjE3MzYxfQ&auto=format&fit=crop&w=1351&q=80
summary: Any website that uses a static generator.

---
前面的內容必須是[降價](https://github.com/jonschlinkert/gray-matter)文件中的第一個內容，必須採用在三點劃線之間設置的有效 YAML 的形式。

```markdown
---
title: Blogging Like a Hacker
lang: en-US
---
```

[在三點](./global-computed.md#frontmatter)劃線之間，可以預定義（以獲取參考），甚至創建您自己的部分自定義[變量](#predefined-variables)。設置組件來訪問變量。

::: 提示 Vue 中的預告片是**的。** :::

## 替代材料格式

此外，VuePress 還支持 JSON 或[TOML](https://github.com/toml-lang/toml)前端。

JSON 前面的內容需要以花的形式和結尾：

    ---
    {
      "title": "Blogging Like a Hacker",
      "lang": "en-US"
    }
    ---

TOML前題需要標註為TOML：

    ---toml
    title = "Blogging Like a Hacker"
    lang = "en-US"
    ---

## 預定義變量

### 標題

* 類型：`string`
* 默認：`h1_title || siteConfig.title`

當前頁面的標題。

### 郎

* 類型：`string`
* 默認：`en-US`

當前頁面的語言。

### 描述

* 類型：`string`
* 默認：`siteConfig.description`

當前頁面的描述。

### 佈局

* 類型：`string`
* 默認：`Layout`

Set the layout component of the current page.

### permalink

* Type: `string`
* Default: `siteConfig.permalink`

Refer to: [Permalinks](./permalinks.md).

### metaTitle

* Type: `string`
* Default: <code>\`${page.title} | ${siteConfig.title}\`</code>

Override the default meta title.

### meta

* Type: `array`
* Default: `undefined`

Specify extra meta tags to be injected:

``` yaml
---
meta:
  - name: description
    content: hello
  - name: keywords
    content: super duper SEO
---
```

## Predefined Variables Powered By Default Theme

### navbar

* Type: `boolean`
* Default: `undefined`

See: [Default Theme Config > Disable the Navbar](../theme/default-theme-config.md#disable-the-navbar).

### sidebar

* Type: `boolean|'auto'`
* Default: `undefined`

See: [Default Theme Config > Sidebar](../theme/default-theme-config.md#sidebar).