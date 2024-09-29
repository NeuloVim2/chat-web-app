<script setup lang="ts">
import IconNotifications from '@/components/icons/IconNotifications.vue'
import IconSettings from '@/components/icons/IconSettings.vue'
import IconUserAccountThumbnail from '@/components/icons/IconUserAccountThumbnail.vue'
</script>
<template>
  <section class="top-bar">
    <div class="account-info">
      <IconUserAccountThumbnail />
      <h2 class="title-large">Name</h2>
    </div>
    <div class="other">
      <IconNotifications />
      <IconSettings />
    </div>
  </section>
</template>

<style scoped>
.top-bar {
  display: flex;
  justify-content: space-between;
  padding-top: 14px;
}

.account-info {
  display: flex;
  align-items: center;

  & h2 {
    margin-left: 16px;
  }
}

.other {
  & svg {
    margin: 0 0 0 16px;
  }
  & svg:is(:hover, :focus) {
    stroke: var(--on-surface-variant);
  }
}
</style>
