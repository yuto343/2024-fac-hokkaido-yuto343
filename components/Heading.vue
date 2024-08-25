<template>
  <div>
    <h1><slot></slot></h1>
  </div>
</template>

<style scoped>
div {
  width: 100%;
  height: 100%;
  display: grid;
  place-items: center;
}
h1 {
  font-weight: bold;
  background: linear-gradient(to right, #ff5722, #d90d57);
  color: transparent;
  -webkit-background-clip: text;
}
</style>
