<script setup lang="ts">
import IconUploadFile from '@/components/icons/IconUploadFile.vue'
</script>

<template>
  <div class="upload-file-container">
    <input id="upload-file" type="file" accept=".png, .jpeg" />
    <label for="upload-file" class="file-upload-button">
      <IconUploadFile />
    </label>
  </div>
</template>

<style scoped>
input[type='file'] {
  display: none;
}

.upload-file-container:focus,
.upload-file-container:hover {
  stroke: var(--on-surface-variant);
}
</style>
