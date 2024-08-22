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
layout: two-cols-with-title
---

# 自己紹介

::left::

<video  class="rounded-5 video" src="./assets/snowboard.mp4" autoplay loop muted />
🗻ルスツリゾート

::right::

名前：中野 祐人

職業：Jamstackエンジニア @PixelGrid

趣味：北海道で🏂、北海道で⛳️

##### 理想の都道府県
北海道（暑くない、 Gいない、梅雨ない、広い、遊び場がいっぱい）

##### 理想の都市
札幌（京都を超えた碁盤の目、ヨドバシカメラでかくなるらしい、美味しいものいっぱい）

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
CodeGridはフロントエンドに携わる人に向けて書かれたWebマガジンです。

<div class="text-4"> 

- 記事は全て社員が書いてます！(たまに寄稿してもらうことも)
- 創刊してから12年！
- 週に1回、3記事が配信！
- 1ヶ月800円(税抜)！
- 12年で記事総数は1781本以上！
- 最初の30日間は無料！

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
layout: two-cols-with-title
---
# web制作ここからでOK！な入門記事

::left::

<img src="./assets/astro.png" alt="Astro" class="p-2" />

::right::
<div class="pl-5">

## 内容

  <div v-click>

  - Astroの特徴
  - 他のフレームワークなどとの比較 
  - コンポーネントの実装
  - 非同期処理の書き方

  から
  </div>
  <div v-click>

  - 外部データからページを生成
  - Content Collectionsの使い方

  まで解説！
  </div>
</div>

---
layout: section
---


<h1 class="flex flex-items-center flex-justify-center gap-10">
<div>Astroの特徴</div>
<div v-click><IconArrowLeft size="40" class="rotate-180"/></div>
<div v-click>アイランドアーキテチャ</div>
</h1>

---
layout: two-cols-with-title
---

# アイランドアーキテクチャ

JavaScriptを読み込む、読み込まないをコンポーネント単位で制御できます。

::left::

<div>
<div class="flex flex-items-center gap-1">
<LogoSvelte size="18" />Counter.svelte
</div>
```svelte {all|3|4-6|8|15-17|0}
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

</div>

::right::

<div>
<div class="flex flex-items-center gap-1">
<LogoAstro size="18" />pages/index.astro
</div>
```astro {0|2,12|11,13}
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
		<div style="height: 200vh"></div>
	</body>
</html>

```
</div>

---


<SlidevVideo autoplay controls muted>
  <source src="./assets/client-visible-demo.mp4" type="video/mp4">
</SlidevVideo>


---
layout: two-cols-with-title
---
# 今すぐ始めるAstro入門

::left::

<img src="./assets/astro.png" alt="Astro" class="p-2" />

::right::

<div class="flex flex-col gap-10">

<div v-click>

## 全12回！
</div>

<div v-click>

## 過去1年でお気に入り数No.1
</div>

<div v-click>

## 僕が書きました。
</div>

</div>
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
