---
hideInToc: true
layout: section
---

## ライブラリを使用するデメリット

<!-- ライブラリを導入するデメリットは他にもたくさんありますが、僕が特に身をもって復旧したこと。を3つ挙げました。 それぞれ見ていくと-->

---

layout: image-right
image: ./assets/polyfill-io.png
backgroundSize: contain
hideInToc: true

---

## 依存性の増加

<div class="pt-10">

- メンテナンスされなくなるかも。

- バグ修正されないかも。

</div>

<!-- 右の図は、Polyfill.ioが中国企業に買収され、マルウェアが注入されたとニューズになった時の画像です-->

## <!-- もし、使用しているライブラリにこのようなことがあれば、 対応に追われてんてこ舞いになることが目に見えています。-->

layout: two-cols-header
hideInToc: true

---

## 学習コストの増加

::left::

```js
import { observable, action, makeObservable } from "mobx";
import { observer } from "mobx-react";

class CounterStore {
  count = 0;

  constructor() {
    makeObservable(this, {
      count: observable,
      increment: action,
      decrement: action,
    });
  }

  increment = () => {
    this.count++;
  };

  decrement = () => {
    this.count--;
  };
}
```

::right::

<div class="pl-6">

- 始めはライブラリのドキュメントを読まないと理解できないことが多い。

- ライブラリの使い方や設計思想を理解するために時間と労力がかかる。

- チーム全員がそのライブラリを習得する必要がある。

</div>
<!-- こちらは、MobXを用いたStoreの実装で、個人的には慣れ親しんでいるライブラリですが、初めて触る人にとっては、分かりにくいはずです。-->
---
layout: image-right
image: ./assets/update-failed.png
backgroundSize: contain
hideInToc: true
---

## バージョンアップの手間

<div class="pt-18">

- バージョンアップの際に、ライブラリ同士の互換性の問題が発生することは日常茶飯事...

- こまめに手をかけておかないと、後からすごい労力になる

</div>

---

layout: fact
hideInToc: true

---

## ライブラリはできるだけ減らせたほうが吉

---

## layout: section

<div class="flex flex-justify-center flex-col gap-10">

<div v-click>

## アイランドアーキテクチャ

  </div>
  
  <div v-click>

## コンテンツ主体のwebサイトに向いた機能性

  </div>
  <div v-click>

## 他のwebフレームワークの言語が使える

  </div>

</div>

---

# コンテンツ主体のwebサイトに向いた機能性

---

## layout: two-cols-header

# Content Collections

ローカルコンテンツのスキーマを定義し、厳密に管理できます。

::left::

<div class="pr-5" v-click>

collections/config.ts

```ts
import { z, defineCollection } from "astro:content";

const writing = defineCollection({
  schema: z.object({
    title: z.string(),
    draft: z.boolean(),
    at: z.string().optional(),
    date: z.date(),
    link: z.string().optional(),
  }),
});

export const collections = {
  writing,
};
```

</div>

::right::

<div v-click>

content/2024-supabase-1.md

```md
---
title: Supabaseで作る記録アプリ | 第1回 プロジェクトの作成と簡単なテーブルの作成
draft: false
at: CodeGrid
date: 2024-08-08
link: https://www.codegrid.net/articles/2024-supabase-1/
---
```

</div>

---

## layout: section

# Zero Lock-in

AstroはメジャーなUIフレームワークをサポートしています。

---

## Zero Lock-in

このように、UIフレームワークのコンポーネントが混在したコードが書けます。

```astro

---
import MyReactComponent from '../components/MyReactComponent.jsx';
import MySvelteComponent from '../components/MySvelteComponent.svelte';
import MyVueComponent from '../components/MyVueComponent.vue';
---
<div>
  <MySvelteComponent />
  <MyReactComponent />
  <MyVueComponent />
</div>
```

---

## 今から始める、Astro入門

このような特徴から、Astroの使い方を、解説しています。全12回です。

- 第1回 Astroの特徴
- 第2回 Astroコンポーネントの実装（2022年8月25日）
- 第3回 UIコンポーネントの導入と実装（2022年9月8日）
- 第4回 クライアントサイドでJavaScriptを動作させる（2022年9月15日）
- 第5回 AstroファイルでのCSSの書き方（2022年10月13日）
- 第6回 UIフレームワークでのスタイリング（2022年10月27日）
- 第7回 Tailwind CSSを利用したスタイリング（2022年11月17日）
- 第8回 Astroで定義した変数をCSSで使う（2022年12月1日）
- 第9回 Astroで非同期処理を扱う（2022年12月15日）
- 第10回 外部データからページを生成する（2023年1月5日）
- 第11回 Markdownファイルの扱い方（2023年2月9日）
- 第12回 Content Collectionsを使う（2023年2月24日）
