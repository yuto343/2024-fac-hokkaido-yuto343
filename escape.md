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
<!-- もし、使用しているライブラリにこのようなことがあれば、 対応に追われてんてこ舞いになることが目に見えています。-->
---
layout: two-cols-header
hideInToc: true
---

## 学習コストの増加


::left::

```js
import { observable, action, makeObservable } from 'mobx';
import { observer } from 'mobx-react';

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


