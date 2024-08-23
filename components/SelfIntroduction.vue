<template>
  <ul class="list">
    <li class="item-s">
      <span class="label">名前</span><span class="content">中野 祐人</span>
    </li>
    <li class="item-s">
      <span class="label">職業</span
      ><span class="content">Jamstackエンジニア@PixelGrid</span>
    </li>
    <li class="item-s">
      <span class="label">趣味</span>
      <span class="content"> 北海道で🏂、北海道で🏌️‍♀️ </span>
    </li>
    <li class="item-l first-lg-item">
      <div class="label-lg">理想の都道府県</div>
      <div class="content">
        北海道 （暑くない、 Gいない、梅雨ない、広い、遊び場がいっぱい）
      </div>
    </li>
    <li class="item-l">
      <div class="label-lg">理想の都市</div>
      <div class="content">
        札幌
        <ul>
          <li>京都を超えた碁盤の目</li>
          <li>ヨドバシカメラ(2028年にでかくなるらしい)</li>
          <li>美味しいものいっぱい</li>
        </ul>
      </div>
    </li>
  </ul>
</template>
<style scoped>
.list {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.item-s {
  list-style: none;
  font-size: 1.3rem;
  display: flex;
  gap: 0.5rem;
}

.item-l {
  padding-top: 0.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
  list-style: none;
  align-items: flex-start;
}
.label {
  display: grid;
  place-items: center;
  line-height: 1;
  padding: 0.1rem 0.5rem;
  background: linear-gradient(to right, #ff5722, #d90d57);
  border-radius: 1rem;
  font-size: 0.9rem;
  font-weight: bold;
}
.label-lg {
  display: grid;
  place-items: center;
  line-height: 1;
  padding: 0.5rem 1rem;
  background: linear-gradient(to right, #ff5722, #d90d57);
  border-radius: 1rem;
  font-size: 0.9rem;
  font-weight: bold;
}
</style>
<script>
export default {
  props: {},
};
</script>
