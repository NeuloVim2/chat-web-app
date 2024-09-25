<script setup lang="ts"></script>
<template>
    <div class="send-message">
        <div class="message-container">
            <img src="../assets/message-image.png" alt="Image from message" class="message-image">
            <p class="bubble-text">Recieved message</p>
        </div>
    </div>
</template>
<style scoped>
.send-message {
    display: flex;
    flex-direction: column;
    align-items: end;
}

.send-message>.message-container {
    display: flex;
    flex-direction: column;
    flex: 0 0 0;
}

.message-image {
    margin-bottom: 4px;
}
</style>