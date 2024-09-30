<script setup lang="ts">
import ChatsListItem from '@/components/ChatsListItem.vue'
import SearchBar from '@/components/SearchBar.vue'
import IconFold from '@/components/icons/IconFold.vue'
import { ref } from 'vue'

const isFolded = ref(false)

const toggleFolded = () => {
  isFolded.value = !isFolded.value
}
</script>
<template>
  <div :className="`folded-section ${isFolded ? 'visible' : ''}`">
    <IconFold @click="toggleFolded" />
  </div>
  <section :className="isFolded ? 'folded' : ''">
    <ul>
      <div class="chat-list-header">
        <h3 class="title-small">Conversations</h3>
        <IconFold @click="toggleFolded" />
      </div>
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
.folded-section {
  display: none;
  &.visible {
    display: block;
    margin-right: 24px;
    padding-left: 24px;
    padding-top: 14px;
  }
}

section {
  padding: 0px;
  height: 100vh;
  margin-right: 24px;

  flex: 0 0 313px;
  transition: flex-basis 0.2s;

  &.folded {
    flex: 0 0 0;
    width: 0;
    margin: 0;
  }
}
ul {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 13px;

  list-style: none;
}

.chat-list-header {
  display: flex;
  padding: 13px 16px;
  justify-content: space-between;

  & svg:is(:hover, :focus) {
    fill: var(--on-surface-variant);
  }
}

h3 {
  width: 100%;
}
</style>
