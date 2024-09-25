<script setup lang="ts"></script>

<template>
  <li>
    <img src="../assets/Thumbnail.png" alt="chat thubnail" />
    <div class="chats-list-item-content">
      <h3 class="font-body-large">Name</h3>
      <span class="font-body-medium">Last message preview</span>
    </div>
    <span class="font-label-small">10 min</span>
  </li>
</template>

<style scoped>
li {
  display: flex;
  align-items: center;
  padding: 8px 16px;
  gap: 16px;

  border: 0.0625rem solid var(--border-color);
  border-radius: 1rem 1rem 0rem 0rem;
}

.caht-list-item-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 0px;
}

.chats-list-item-content,
span,
div {
  color: var(--on-surface-variant);
}

.chats-list-item-content h3 {
  color: var(--on-surface);
}

li > span {
  width: 37px;
}

/* li > span {
  text-align: center;
  align-self: center;
} */
</style>