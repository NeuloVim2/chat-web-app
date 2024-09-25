<script setup lang="ts">
</script>

<template>
  <div class="search-bar-container">
    <input class="search-bar  placeholder-font-body-large" type="text" placeholder="Hinted search text" />
  </div>
</template>

<style scoped>
.search-bar-container {
  width: 100%;
  padding: 8px 16px;
}
input.search-bar {
  width: 100%;
  padding: 10.5px 10.5px;
  border: solid var(--surface-container-high);
  border-radius: 28px;

  color: var(--on-surface-variant);

  background-color: var(--surface-container-high);
  background-image: url('../assets/icon.png');
  background-repeat: no-repeat;
  background-origin: content-box;
  background-position: right;
}
input.placeholder-font-body-large::placeholder {
 color: var(--on-surface-variant);
 padding-left: 10px;
}
</style>
