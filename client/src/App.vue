<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import ChatsList from './components/ChatsList.vue'
import ConversationSection from './components/ConversationSection.vue'
</script>

<template>
  <ChatsList />
  <ConversationSection />
</template>

<style scoped></style>
