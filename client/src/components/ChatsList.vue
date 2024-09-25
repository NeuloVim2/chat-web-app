<script setup lang="ts">
import ChatsListItem from '@/components/ChatsListItem.vue'
import SearchBar from '@/components/SearchBar.vue'
</script>

<template>
  <section>
    <ul>
      <h3 class="title-small">Conversations</h3>
      <SearchBar />
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
  padding: 0px;
  height: 100vh;

  flex: 0 0 313px;
}
ul {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 13px;

  list-style: none;
}
h3 {
  width: 100%;
  padding: 13px 16px;
}
</style>
