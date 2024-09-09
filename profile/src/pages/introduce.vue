<template>
    <v-container class="fill-height">
      <v-card class="d-flex flex-row" elevation="3" style="padding: 20px; width:100%; margin: 0 auto;">
        <!-- 自我介紹 -->
        <div style="flex: 1; margin-right: 20px;">
          <v-card-title>
            <h1>自我介紹</h1>
          </v-card-title>
          <v-card-text>
            <h3>個性</h3>
            <p>我是個比較文靜內向的人，從小就不喜歡當中心人物或是被當作焦點，但這不代表在小組當中我不會表達自己的想法與意見，只是比較不擅長當領導者。</p>
            <br>
            <p>興趣是很普遍的聽音樂、看動漫、玩遊戲。</p>
            <br>
            <p>最喜歡的動漫是獵人。</p>


            <h3>學習歷程</h3>
            <p>在大學前，我沒有接觸過任何程式語言，高中時找不到自己嚮往的方向，所以選了電機系。</p>
            <br>
            <p>在電機系大一接觸到C語言，當時就有稍微感受到有比同儕多一點天分，加上對於電類一竅不通也沒興趣，猶豫了些許，最後在大二下申請轉系到資工系。</p>
            <br>
            <p>在資工系，我開始接觸到前後端、深度學習、圖像辨識等，也很幸運地遇到了志同道合的朋友，在升大四的暑假自學了Vue2/3以及JavaScript的後端(prisma)，並且自己嘗試寫了一些小作品，詳細部分在專案展示區。</p>


            <h3>未來規劃</h3>
            <p>目前我正在準備收尾模擬代購網站以及學校的專題，預計做完之後會尋找大四下實習的機會(目前估計四下只會修5學分，可以一周實習四天)，而在這期間，我會想學習tailwind以及有關於前後端的知識，如果有多餘時間，會再仔細學習Vue相關的知識。</p>
            <a href="https://roadmap.sh/frontend" target="_blank">前端學習圖(從基礎的html到測試開發再到包裝成app)</a>
            <br>
            <a href="https://roadmap.sh/vue" target="_blank">Vue學習圖</a>
          </v-card-text>
        </div>
        
        <!-- 照片 -->
        <div style="width: 200px; text-align: center;">
          <v-img
            :src="imagepath" 
            alt="個人照片"
            max-width="200"
            class="rounded-circle"
          />
        </div>
      </v-card>
  

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
  import meImagePath from '@/assets/Me.png'
  const router = useRouter();
  const imagepath =meImagePath

  function goBack() {
    router.back();
  }
  </script>
  
  <style scoped>
  h1 {
    font-size: 36px;
    font-weight: bold;
  }
  
  h3 {
    font-size: 32px;
    font-weight: 500;
    margin-bottom: 10px;
  }
  
  p {
    font-size: 20px;
    color: rgb(215, 198, 198)
  }
  
  .v-card {
    max-width: 1200px; 
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
  