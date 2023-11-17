<template>
  <Container :width="600">
    <div class="Experienced">
      <h3>學習經歷</h3>
      <div class="content" v-for="learn in learns" :key="learn.id">
        <div class="year">
          <span> {{ learn.years }} </span>
        </div>
        <div class="work">
          <a v-if="learn.link" :href="learn.link" target="_blank">{{
            learn.title
          }}</a>
          <p v-else>{{ learn.title }}</p>
          <p>
            {{ learn.description }}
          </p>
          <p>{{ learn.skill }}</p>
        </div>
      </div>
      <h3>工作經歷</h3>
      <div class="content" v-for="work in works" :key="work.id">
        <div class="year">
          <span> {{ work.years }} </span>
        </div>
        <div class="work">
          <a v-if="work.link" :href="work.link" target="_blank">{{
            work.title
          }}</a>
          <p v-else>{{ work.title }}</p>
          <p>
            {{ work.description }}
          </p>
          <p>{{ work.skill }}</p>
        </div>
      </div>
    </div>
  </Container>
</template>
<script setup>
import Container from "./Container.vue";

import { ref } from "vue";

const learns = ref([
  {
    id: 1,
    years: "2022.01 - 2022.06",
    title: "UIUX互動式網站UI/UX設計師就業養成班",
    link: "",
    description:
      "畢業一年後，我專注於UI/UX和前端開發。精通AI、PS、Figma，並具備使用者分析和流程規劃能力。在前端，我熟練於HTML、CSS、JQuery和JavaScript，也了解MySQL和PHP。我致力於結合設計與技術創造優質網頁體驗。",
    skill: "Figma • HTML • CSS • jQuery • JavaScript • PHP • mySQL",
  },
  {
    id: 2,
    years: "2016.08 - 2020.06",
    title: "中國科技大學數位多媒體",
    link: "",
    description:
      "主修3D建模、2D繪圖、平面視覺，選修影片剪輯、UIUX、AE特效。畢業專題中擔任組長，負責主角3D建模和動畫製作，有效整合組員資訊，並與教授合作確定開發方向。",
    skill: "Adobe effect • Photoshop • illustrator • Premiere • Blender",
  },

  // 可以繼續添加更多項目
]);
const works = ref([
  {
    id: 1,
    years: "2022.07 - 2023.08",
    title: "光曜町數位行銷 - Hikaru Digital Marketing",
    link: "https://www.hikaru.com.tw/",
    description:
      "在光曜町數位行銷的一年工作經歷中，我不僅負責網頁維護，還參與一頁式網站、官方網站、Line內互動網頁及 CMS 後台的UI/UX設計與前端開發。我熟練掌握HTML、CSS、jQuery和JavaScript，與設計團隊緊密合作，致力於提升用戶體驗和滿足客戶需求。我的技能涵蓋從界面設計到功能實現，展現了我在前端開發領域的專業能力與多元化。",
    skill: "Figma • HTML • CSS • jQuery • JavaScript • GSAP • RESTful API",
  },
  // 可以繼續添加更多項目
]);
</script>
<style scoped>
.content,
.Experienced {
  color: white;
}

.Experienced {
  margin-top: 30px;
  line-height: 24px;
}

.Experienced > h3 {
  text-align: center;
  margin-top: 40px;
  margin-bottom: 16px;
}

.content {
  display: flex;
  justify-content: center;
  gap: 34px;
  margin: 24px 0;
}

.year {
  text-align: right;
  flex: d 0 130px;
  word-wrap: normal;
  color: rgba(255, 255, 255, 0.527);
}
@media screen and (max-width: 525px) {
  .content {
    flex-wrap: wrap;
    gap: 10px;
  }
  .year {
    text-align: left;
    flex: 1 1 100%;
  }
}

.work {
  flex: 2 1 300px;
  text-align: left;
  line-height: 24px;
  text-align: justify;
}

.work a,
p:nth-child(1) {
  color: rgba(255, 255, 255);
  font-weight: 900;
}

.work p:nth-child(2) {
  color: rgba(255, 255, 255, 0.7);
  margin: 10px 0;
}

.work p:nth-child(3) {
  color: rgba(255, 255, 255, 0.5);
}
</style>
