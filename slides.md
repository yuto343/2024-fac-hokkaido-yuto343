---
# You can also start simply with 'default'
theme: ./theme
# some information about your slides (markdown enabled)
title: CodeGrid記事かいつまみ紹介

class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
hideInToc: true
---

# CodeGrid記事かいつまみ紹介

<p class="text-right">Yuto Nakano</p>
<p class="text-right">2024.08.24 フロントエンドカンファレンス北海道</p>

---
hideInToc: true
---
# 目次

<Toc columns=2 />

<!--
- はじめにCodeGridとは？どんな記事が読めるのか?という部分を紹介しながら、
- おすすめしたいきじをごしょうかいさせていただきます
-->

---
title: CodeGridとは?
---

<Heading>CodeGridとは？</Heading>

<!--
- 本番では知っている人、購読してくれている人、みたいなのを聞く
-->

---
layout: image-left
image: ./assets/codegrid.png
backgroundSize: contain
hideInToc: true
---

## CodeGrid基本情報
CodeGridは、フロントエンドに携わる人に向けて書かれたWebマガジンです。

<div class="text-6"> 

- 創刊してから12年！
- 週に1回、3記事が配信！
- 1ヶ月800円！
- 12年で記事総数は1781本！

</div>

<!-- 実際はどんな記事が読めるのか、ワードクラウドを作りました。 -->
---
layout: section
---

## どんな内容の記事が読めるの？

---
layout: image
image: ./assets/wordcloud-1.png
---

<!-- 
この画像は、CodeGridのカテゴリーごとの記事数から、記事数が多いもののフォントがが大きく、記事数が少ないものが小さくなるように作ったワードクラウドです。
なので、どのような記事が多いのかを視覚的に表現しています。
この画像を細かく見ていきます。
-->

---
layout: image-left
image: ./assets/wordcloud-2.png
backgroundSize: contain
---

## 実践記事が多い
CodeGridは、エンジニアが日々の業務の中で得た知見を元に書かれていることが多く、「活きた」情報が得られます。

<span>📚 例えば... </span>
- ライブラリなしで実装する定番UI
- 初心者のためのコードレビューファーストステップ
- 読みやすいコードを書くためのヒント

---
layout: section-with-subtitle
---

## ライブラリなしで実装する定番UI

::subtitle::
📖 記事かいつまみ紹介

---
hideInToc: true
---

# ライブラリを使わずに実装する定番UI
このシリーズでは全31回で、以下のUIをライブラリなしで実装する方法を紹介しています。

- ドロワーナビ
- ローディング画面
- スティッキーナビ
- タブUI
- カルーセルUI
- セレクトボックス
- ツリービュー

<!-- カルーセルなどは、ライブラリを導入して作るUIの定番ですが、この記事を読めばライブラリを使わずに実装できるようになります。
それぞれアクセシビリティにも配慮された作りになっているので、その点でも非常に参考になるシリーズです。
 -->

---
layout: image-right
image: ./assets/wordcloud-3.png
backgroundSize: contain
---

## ライブラリや、Webフレームワークの記事も豊富

使い方を説明した入門記事から、ひとつの機能にフォーカスして深掘りした記事まで、幅広い内容が揃っています。

<div class="pt-5">

<span>📚 例えば... </span>
- 今すぐ始めるAstro入門
- これから始める、Next.js
- Preactで始める軽量コンポーネント指向開発
- SWRで快適！ Reactでのデータ取得
- SvelteKit入門
- Vue 3から始める、Vue.js

</div>

<style>
h1 {
  /* text-wrap:nowrap */
}
</style>

<!-- 流行りのライブラリやWebフレームワークの記事も豊富です -->
---
layout: section-with-subtitle
---

## 今すぐ始めるAstro入門

::subtitle::
📖 記事かいつまみ紹介

---
layout: section
---

## Astroとは？

---
layout: iframe-left
url: https://astro.build/
---

## 特徴

<div class="text-6 pt-5">

  <div v-click>
  - 
  </div>
  <div v-click>
  - Astroアイランド
  </div>
  <div v-click>  
  - Zero Lock-in
  </div>

</div>
---
layout: section
---

# for content-driven websites
メディアサイトなど、コンテンツが主体となったwebサイトを作るのに適したフレームワークです。

<!-- そのコンテンツ管理の特徴的な機能としてContent Collectionsがあります。 -->
---
layout: two-cols-header
---

# Content Collections
ローカルコンテンツのスキーマを定義し、厳密に管理できます。

::left::

<div class="pr-5" v-click>

collections/config.ts
```ts
import { z, defineCollection } from "astro:content"

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
  writing
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
layout: section
---

# Astro Islands

JavaScriptを読み込む、読み込まないをコンポーネント単位で制御できます。

---
layout: two-cols
---

Counter.svelte
```svelte
<script>
  import { onMount } from "svelte";

  let count = 0;

  function countUp() {
    count += 1;
  }

  onMount(() => {
    const interval = setInterval(countUp, 1000);

    return () => {
      clearInterval(interval);
    };
  });
</script>

<div>
  Count：{count}
</div>
```

::right::

<div v-click>

pages/index.astro

```astro
---
import Counter from "../components/counter.svelte";
---

<html lang="en">
	<head>
		<meta charset="utf-8" />
	</head>
	<body>
		<h1>スクロールしてね</h1>
		<div style="height: 200vh"></div>
		<Counter client:visible />
	</body>
</html>

```
</div>
---

<SlidevVideo autoplay controls>
  <source src="./assets/client-visible-demo.mp4" type="video/mp4">
</SlidevVideo>
---
layout: section
---

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

---
layout: image-right
image: ./assets/wordcloud-4.png
backgroundSize: contain
---

## 実は、技術以外の記事も豊富

実は、ディレクター、デザイナー、社長の視点で書かれた記事、インタビューなどの読み物としてただ楽しめる記事も多いです。

<div class="pt-5">

<span>📚 例えば... </span>
- ピクセルグリッドの仕事術
- ピクセルグリッドが訪ねる、開発の現場
- 気になる余白と気になりにくい余白
- きちんと学ぶユーザーインターフェース
- エンジニアが知っておきたい仕事のお作法
- GitHub Projectsを使った業務管理

</div>

--- 
layout: section-with-subtitle
hideInToc: true
---

## ピクセルグリッドの仕事術

::subtitle::
📖 記事かいつまみ紹介

---

## ピクセルグリッドにはユニークな制度がたくさん。

<div class="text-8 pt-10" v-click>

- パーソナルトレーニング
- 名刺のデジタル化
- 利益を山分けするボーナス制度
- 就業時間のない会社
- etc...

</div>

---
layout: section
---

## これらが、どのような考えから生まれ、どのように運用されているのか、その裏側が紹介されています。

---

## 例えば...

<div class="pt-5">

### パーソナルトレーニング
- なぜ、フィットネスジムへの補助ではないのか？
- 実験的に実施した際のスタッフの反応は？

</div>

<div class="pt-5">

### 名刺のデジタル化
- 既存のサービスを使わず、独自に開発した理由は？

</div>

<div class="pt-5">

### 利益を山分けするボーナス制度
- 不公平のないように、どういう計算で決められているのか？

</div>


---
layout: two-cols-header
---

## ピクセルグリッドの仕事術
このようなピクセルグリッドのユニークな制度や、仕組みなどのノウハウを紹介。全34回。

::left::
<div class="text-3">

- 第1回 JavaScript開発見積もり（2012年6月14日）
- 第2回 ポイントによる見積もり（2012年6月21日）
- 第3回 人材採用（2012年9月27日）
- 第4回 報酬とはなにか？（2012年10月4日）
- 第5回 給料体系（2012年10月11日）
- 第6回 個人利益を確保する待遇（2012年10月18日）
- 第7回 就業時間のない会社（2013年2月14日）
- 第8回 電話のない会社（2013年4月11日）
- 第9回 経営理念を考える（2013年11月14日）
- 第10回 通勤時間と働きやすさ（2014年3月13日）
- 第11回 ピクセルグリッドの面談（2014年6月26日）
- 第12回 特化するということ（2014年7月24日）
- 第13回 「作る」をやめない（2014年9月11日）
- 第14回 理想の会社を実験する（2014年11月27日）
- 第15回 値下げと適正価格（2015年1月8日）
- 第16回 社内サーバーを置かない（2015年3月26日）
- 第17回 「仲のよい」組織を作る（2015年8月13日）
- 第18回 経理業務フローの効率化（2015年11月5日）
- 第19回 内製と外部発注（2015年11月26日）

</div>
::right::

<div class="text-3">

- 第20回 会社の組織構造（2016年2月4日）
- 第21回 よりよい仕組みに乗り換える（2016年7月21日）
- 第22回 無借金での経営（2016年10月20日）
- 第23回 余裕がある会社（2017年2月9日）
- 第24回 リモートワークの形態と運営のコツ（2017年3月9日）
- 第25回 面接と採用の仕組み（2017年5月25日）
- 第26回 人を増やすということ（2017年8月31日）
- 第27回 わかりやすい文章を大切にする（2017年10月26日）
- 第28回 連絡手段を選ぶ（2018年6月7日）
- 第29回 会社として運動不足に立ち向かう（2018年8月9日）
- 第30回 求人コンテンツの見直し（2019年8月29日）
- 第31回 インプットする時間を確保する（2020年4月23日）
- 第32回 フラットな関係を維持する努力（2020年11月19日）
- 第33回 ボーナスのしくみ（2021年7月15日）
- 第34回 名刺のデジタル化（2024年5月30日）

</div>

---
layout: section
---

# 以上、もし気になりましたら、是非CodeGridをよろしくお願いします！

<style>
h1 {
  font-size: 2rem;
}
</style>
