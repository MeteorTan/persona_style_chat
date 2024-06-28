<template>
  <div class="chatroom_background">
    <ChatMessage v-for="(item, index) in chatList" :key="index" :isMe="item.id % 2" 
    :content="item.message_content">
    </ChatMessage>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import ChatMessage from './ChatMessage.vue';

const chatList = ref([{ "id": 1, "message_content": "1tkJUFoN6n2BsSwBxXShCkr2pzKVPJWeU" },
{ "id": 2, "message_content": "18JJbj1kMRq9RK5SxubCb39xMf4PRbFdks" },
{ "id": 3, "message_content": "19X6ZogegNZYAxYkBGVGgRmCrNwynmDGV7" },
{ "id": 4, "message_content": "16FoHGxNyGP823ELyGmuxQqarPyEGbCLz4" },
{ "id": 5, "message_content": "12UsXArMYDvV69X4ZR8HpUQQFXZmLAW945" },
{ "id": 6, "message_content": "15VyKDPhkyAgfdjQLfiyGYU7vkqdodKExu" },
{ "id": 7, "message_content": "16dLeJroNTa3TR2f5dfNd8eStdWpMiSD49" },
{ "id": 8, "message_content": "1PSnKFWstGSjNu5gMaCFkzaxv6uCYmphmg" },
{ "id": 9, "message_content": "1Jq7uJ1yyh4ubMZ5PTAfg8MqPLPXyTQLbh" },
{ "id": 10, "message_content": "17z7KSXU9uyvFt43r8wZcHYNB9gBaANJdN" },
{ "id": 11, "message_content": "12EQr79LGvu2kjjUfjNh5xjySfqe6kjV6z" },
{ "id": 12, "message_content": "13ocezeGCWpePqunXkMDfMqhDX9creY5ET" },
{ "id": 13, "message_content": "1DAL6wKTEoxfZS8yXfZ7NUztzmzfCi5ugg" },
{ "id": 14, "message_content": "1LZ31pzcQiAU8n6Npbj5CifhYJ3TZ6KuNN" },
{ "id": 15, "message_content": "1KLf5YFecsEcvzSaMCWGyxFRgUQw3Mxxxq" },
{ "id": 16, "message_content": "1PumcCHdpzYzFghJdfBQew4FGesz5H6MT7" },
{ "id": 17, "message_content": "18TYHTVPMHBr27VaC1245kKKvCin6nZKG7" },
{ "id": 18, "message_content": "1NaqwwP8ghYsZrRfHyZrzendoHCrY1wvMw" },
{ "id": 19, "message_content": "19M1MPmtVV85E4KFqXappUNF3Vy3yyf592" },
{ "id": 20, "message_content": "1po6xFfpQhTSCuAWV428gCzH2qfjM1yr5" },
{ "id": 21, "message_content": "1NVDKFM1RyyA1eS6mwS5HTcrV6wgVsxRoK" },
{ "id": 22, "message_content": "1Lf45zMREgqKM5JHbcUZHM1EQaMdyFg9V" },
{ "id": 23, "message_content": "1BFEiwtZUhoHxGPxvjuq7TxvK5jdSRoU5s" },
{ "id": 24, "message_content": "1FtvqiREUbwoaXsDxGXv1YpFnTRsd2hh8B" },
{ "id": 25, "message_content": "1EgFzx25e5cFkwiuoo8WDpsqvkoNzaGDvm" },
{ "id": 26, "message_content": "1FstY3wqmQTp1wex1cZLDpSruJeRvJEoGb" },
{ "id": 27, "message_content": "1J1JNpRMbzjmiFnguxLQgv3uqXJmrcNfvf" },
{ "id": 28, "message_content": "1KmDbRjWPPPXxPCnGZ3CvPU9Ai87Z57wxr" },
{ "id": 29, "message_content": "1JYaXfnKjybEd4yYvFqxppVm7nPdahKH64" },
{ "id": 30, "message_content": "12QbTBgz3gQxx3EDAnFEPJ8hQFtZ9ZtQ5m" }]);
</script>

<style scoped>
.chatroom_background {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 600px;
  height: 800px;
  background: red;
  padding: 20px;
  overflow: scroll;
}
</style>