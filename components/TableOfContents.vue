<template>
  <ol class="list1">
    <li class="item1">
      <p class="title1">1. CodeGridとは?</p>
      <span class="note1">CodeGridの基本情報の紹介</span>
    </li>
    <li class="item1">
      <p class="title1">2. どんな内容の記事が読めるの？</p>
      <span class="note1">ワードクラウドを元に、どんな記事があるか紹介</span>
      <ol class="list2">
        <li>
          <p class="title2">① 実践記事が多い</p>
          <ul class="list3">
            <li class="item3">
              <span class="note2">記事紹介</span>
              <p class="title3">ライブラリなしで実装する定番UI</p>
            </li>
          </ul>
        </li>
        <li>
          <p class="title2">③ ライブラリ・webフレームワークの記事も豊富</p>
          <ul class="list3">
            <li class="item3">
              <span class="note2">記事紹介</span>
              <p class="title3">今すぐ始めるAstro入門</p>
            </li>
          </ul>
        </li>
        <li>
          <p class="title2">③ 実は技術以外の記事も豊富</p>
          <ul class="list3">
            <li class="item3">
              <span class="note2">記事紹介</span>
              <p class="title3">ピクセルグリッドの仕事術</p>
            </li>
          </ul>
        </li>
      </ol>
    </li>
    <li class="item1 last">
      <p class="title1">3. おみやげ</p>
    </li>
  </ol>
</template>
<style scoped>
p {
  margin: 0;
}
.list1 {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.title1 {
  font-weight: bold;
  background: linear-gradient(to right, #ff5722, #d90d57);
  color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  padding: 1px;
  clip-path: inset(1px);
  font-size: 1.75rem;
}
.note1 {
  opacity: 0.5;
  padding-left: 0.5rem;
}
.list2 {
  padding-left: 1rem;
  padding-top: 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.title2 {
  font-weight: bold;
  background: linear-gradient(to right, #ff5722, #d90d57);
  color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  padding: 1px;
  clip-path: inset(1px);
  font-size: 1.5rem;
}
.note2 {
  padding: 0.2rem 0.7rem;
  background: linear-gradient(to right, #ff5722, #d90d57);
  border-radius: 0.8rem;
  font-size: 0.8rem;
  line-height: 1;
  font-weight: bold;
}
.list3 {
  padding-top: 0.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.item3 {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.title3 {
  font-size: 1.2rem;
}
.last {
  padding-top: 0.5rem;
}
</style>
<script>
export default {
  props: {},
};
</script>
