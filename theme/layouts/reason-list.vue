<template>
  <div class="w-full h-full flex flex-items-center flex-justify-center">
    <div class="container">
      <div class="sidebar">
        <ul>
          <li
            v-for="(item, index) in items"
            :key="index"
            :class="{ active: selectedIndex === index }"
            @click="selectItem(index)"
          >
            {{ item.title }}
          </li>
        </ul>
      </div>
      <div class="content">
        <div v-if="selectedIndex !== null">
          <h2>{{ items[selectedIndex].title }}</h2>
          <p>{{ items[selectedIndex].description }}</p>
          <img
            :src="items[selectedIndex].image"
            alt=""
            v-if="items[selectedIndex].image"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedIndex: 0,
      items: [
        {
          title: "依存性の増加",
          description: "依存性の増加に関する説明テキスト。",
          image: "path/to/dependency-image.jpg",
        },
        {
          title: "学習コスト",
          description: "学習コストに関する説明テキスト。",
          image: "path/to/learning-cost-image.jpg",
        },
        {
          title: "バージョンアップの手間",
          description: "バージョンアップの手間に関する説明テキスト。",
          image: "path/to/version-upgrade-image.jpg",
        },
      ],
    };
  },
  methods: {
    selectItem(index) {
      this.selectedIndex = index;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
}

.sidebar {
  width: 30%;
  background-color: #f4f4f4;
  padding: 10px;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  padding: 10px;
  cursor: pointer;
}

.sidebar li.active {
  background-color: #ddd;
  font-weight: bold;
}

.content {
  width: 70%;
  padding: 10px;
}

.content img {
  max-width: 100%;
  height: auto;
}
</style>
