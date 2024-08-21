<template>
  <div>
    <button @click="toggleSection(1)">Toggle Section 1</button>
    <button @click="toggleSection(2)">Toggle Section 2</button>
    <button @click="toggleSection(3)">Toggle Section 3</button>

    <div v-if="visibleSection === 1">
      <h2>Section 1</h2>
      <p>Content for section 1...</p>
    </div>

    <div v-if="visibleSection === 2">
      <h2>Section 2</h2>
      <p>Content for section 2...</p>
    </div>

    <div v-if="visibleSection === 3">
      <h2>Section 3</h2>
      <p>Content for section 3...</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visibleSection: 1,
    };
  },
  methods: {
    toggleSection(section) {
      this.visibleSection = section;
    },
  },
};
</script>

<style scoped>
button {
  margin-right: 10px;
}
</style>