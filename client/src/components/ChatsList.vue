<script setup lang="ts">
import ChatsListItem from '@/components/ChatsListItem.vue'
import SearchBar from '@/components/SearchBar.vue'
</script>

<template>
  <section>
    <SearchBar />
    <ul>
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
    </ul>
  </section>
</template>

<style scoped>
section {
  border: 0.001rem solid white;
}
ul {
  list-style: none;
}
</style>
