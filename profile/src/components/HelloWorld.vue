<template>
  <v-container >
    <v-card class="header-card" elevation="3">
      <v-card-title class="text-center">
        <h1>{{ siteTitle }}</h1>
      </v-card-title>
      <v-card-subtitle class="text-center">{{ subtitle }}</v-card-subtitle>
    </v-card>

    <v-card class="mt-6" elevation="3">
      <v-card-title class="text-center">
        <h1>關於我</h1>
      </v-card-title>
      <v-card-text>
        <p style="font-weight: 300; font-size: 20px; line-height: 1.6;">
          {{ aboutText1 }}
        </p>
        <ul style="font-weight: 300; font-size: 16px; line-height: 1.6; color: rgb(211, 211, 157);">
          <li v-for="lan in languageInSchool" :key="lan">
            {{ lan }}
          </li>
          <br>
          <li v-for="lan in languageSelf" :key="lan"> 
            {{ lan }}
          </li>
        </ul>
        <br>
        <a href="http://localhost:3000/introduce" style="color: rgb(159, 184, 231); text-decoration: underline;">
          更多有關於我的自我介紹
        </a>
        
      </v-card-text>
    </v-card>
    

    <v-card class="mt-6" elevation="3">
      <v-card-title class="text-center">
        <h1>作品集</h1>
      </v-card-title>
      <v-card-text>
        <v-row>
          <v-col
            v-for="(project, index) in projects"
            :key="index"
            cols="12"
            md="4"
          >
            <v-card>
              <v-img :src="project.image" height="200px"></v-img>
              <v-card-title>{{ project.title }}</v-card-title>
              <v-card-subtitle>{{ project.description }}</v-card-subtitle>
            </v-card>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';


const siteTitle = ref('我的個人網站');
const subtitle = ref('全端開發者 | 程式設計師');


const aboutText1 = ref('你好，我是巫旼學，目前就讀長庚大學資工系大四，以下是我學習過的程式語言');
const languageInSchool = ref(['大學中學習的','C/C++','Java','Python']);
const languageSelf = ref(['自學的','React','Vue2/Vue3','js(前後端)']);



const projects = ref([
  { title: '專案 1', description: '描述 1', image: 'https://via.placeholder.com/400x200' },
  { title: '專案 2', description: '描述 2', image: 'https://via.placeholder.com/400x200' },
  { title: '專案 3', description: '描述 3', image: 'https://via.placeholder.com/400x200' }
]);


const contactForm = ref({
  name: '',
  email: '',
  message: ''
});
</script>

<style scoped>
.header-card {
  margin-bottom: 20px;
  padding: 30px;
}

.fill-height {
  min-height: 100vh;
}

.v-card {
  margin-bottom: 20px;
}

.text-center {
  text-align: center;
}
</style>

