<script setup lang="ts">
import SendMessage from '@/components/SendMessage.vue'
import ReplyMessage from '@/components/ReplyMessage.vue'
import TopBar from '@/components/TopBar.vue'
import MessageInput from '@/components/MessageInput.vue'
</script>

<template>
  <main class="conversation">
    <div class="container">
      <TopBar />
      <section class="content">
        <SendMessage />
        <ReplyMessage />
        <ReplyMessage />
        <ReplyMessage />
      </section>
      <MessageInput />
    </div>
  </main>
</template>

<style scoped>
main.conversation {
  margin-left: 24px;
  flex: 1 1 100%;
  background-color: var(--surface-container-lowest);
  min-height: 100%;
}

.conversation > .container {
  padding: 0 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 42px;
  height: 100vh;
  margin-bottom: 24px;
}

.content {
  flex: 1 1 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 8px;
}
</style>
