<script setup lang="ts"></script>

<template>
  <li>
    <img src="../assets/Thumbnail.png" alt="chat thubnail" />
    <div class="chats-list-item-content">
      <h3>Name</h3>
      <span>Last message preview</span>
    </div>
    <div>10 min</div>
  </li>
</template>

<style scoped>
li {
  display: flex;
  width: 100%;
  border: 0.0625rem solid var(--border-color);
  border-radius: 1rem 1rem 0rem 0rem;
}
.chats-list-item-content {
}
</style>
