<script setup lang="ts">
import ChatsListItem from '@/components/ChatsListItem.vue'
import SearchBar from '@/components/SearchBar.vue'
</script>

<template>
  <section>
    <span>Conversations</span>
    <SearchBar />
    <ul>
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
      <ChatsListItem />
    </ul>
  </section>
</template>

<style scoped>
section {
  min-height: 100vh;
  border: 0.00001rem solid white;
  max-width: 20vw;
}
ul {
  list-style: none;
}
</style>
