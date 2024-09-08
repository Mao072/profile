<template>
    <v-container class="fill-height">
      <v-card class="d-flex flex-row" elevation="3" style="padding: 20px; width:100%; margin: 0 auto;">
        <!-- 左邊的內容區域 -->
        <div style="flex: 1; margin-right: 20px;">
          <v-card-title>
            <h1>大標題</h1>
          </v-card-title>
          <v-card-text>
            <h3>小標題 1</h3>
            <p>這是一段關於小標題1的描述內容。</p>
            
            <h3>小標題 2</h3>
            <p>這是一段關於小標題2的描述內容。</p>
            
            <h3>小標題 3</h3>
            <p>這是一段關於小標題3的描述內容。</p>
          </v-card-text>
        </div>
        
        <!-- 右邊的照片區域 -->
        <div style="width: 200px; text-align: center;">
          <v-img
            src="https://via.placeholder.com/150" 
            alt="個人照片"
            max-width="150"
            class="rounded-circle"
          />
          <p>這裡是放置個人照片的區域</p>
        </div>
      </v-card>
  
      <!-- 回到上一頁的按鈕 -->
      <v-btn
        fab
        dark
        @click="goBack"
        class="back-button"
      >
        <v-icon>mdi-arrow-left</v-icon>
      </v-btn>
    </v-container>
  </template>
  
  <script lang="ts" setup>
  import { useRouter } from 'vue-router';
  
  const router = useRouter();
  
  function goBack() {
    router.back(); // 返回上一頁
  }
  </script>
  
  <style scoped>
  h1 {
    font-size: 36px;
    font-weight: bold;
  }
  
  h3 {
    font-size: 24px;
    font-weight: 500;
    margin-bottom: 10px;
  }
  
  p {
    font-size: 16px;
    color: #555;
  }
  
  .v-card {
    max-width: 1200px; /* 最大寬度 */
  }
  
  .v-img {
    border-radius: 50%;
    border: 2px solid #ccc;
  }
  
  .back-button {
    position: fixed;
    right: 20px;
    bottom: 20px;
  }
  </style>
  