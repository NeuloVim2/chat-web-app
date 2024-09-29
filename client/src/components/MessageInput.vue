<script setup lang="ts">
import { onMounted, useTemplateRef } from 'vue'
import FileUpload from '@/components/FileUpload.vue'
import IconSendMessage from '@/components/icons/IconSendMessage.vue'
import IconEmoji from '@/components/icons/IconEmoji.vue'
// import { useTextareaAutosize } from '@vueuse/core';

const textarea = useTemplateRef('textarea')

onMounted(() => {
  const maxHeight = getComputedStyle(textarea.value as Element).maxHeight

  textarea.value?.addEventListener('input', () => {
    if (textarea.value) {
      textarea.value.style.height = 'auto'
      textarea.value.style.overflow = 'none'

      textarea.value.style.height = `${textarea.value.scrollHeight}px`

      if (textarea.value.style.height >= maxHeight) textarea.value.style.overflow = 'auto'
    }
  })
})
</script>

<template>
  <section class="message-input">
    <button class="emoji-button">
      <IconEmoji />
    </button>
    <div class="input-container">
      <textarea
        ref="textarea"
        class="message-input-field"
        name="message-input-field"
        id="input-field"
      ></textarea>
      <FileUpload />
    </div>
    <button>
      <IconSendMessage />
    </button>
  </section>
</template>

<style scoped>
.message-input {
  display: flex;
  flex: 1 1 0%;

  & button {
    background-color: var(--surface-container-lowest);
    border: none;
    padding: 16px;
    margin-top: auto;
  }
}

.input-container {
  flex: 1 1 0%;
  display: flex;
  border: none;
  background-color: var(--surface-container-high);
  border-radius: 28px;
  padding: 12px;
  align-items: end;
  height: 100%;

  & textarea {
    border: none;
    background-color: var(--surface-container-high);
    color: var(--on-surface-variant);
    flex: 1 1 0%;
    resize: none;
    overflow: hidden;
    max-height: 175px;
    margin: 0 10px 0 10px;
    scrollbar-color: #5b5b5b transparent;
  }
  & textarea:focus {
    outline: none;
    caret-color: white;
  }
}
</style>
