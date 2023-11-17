<template>
  <Container :width="600">
    <div class="list">
      <div class="listThing" v-for="content in contents">
        <div class="imgBox">
          <img v-if="content.img" :src="imgSrc(content.img)" alt="" />
        </div>
        <p v-if="!content.link">
          {{ content.title }}
        </p>
        <a v-else :href="content.link" target="_blank">{{ content.title }} </a>
        <span class="remark">{{ content.remark }}</span>
        <p>{{ content.text }}</p>
        <div class="skill">
          <div v-for="skill in content.skills" :key="skill" class="tag">
            <p>{{ skill }}</p>
          </div>
        </div>
      </div>
    </div>
  </Container>
</template>
<script setup>
import Container from "./Container.vue";
import { ref } from "vue";

function imgSrc(imgName) {
  return new URL(`../assets/profile_img/${imgName}.jpg`, import.meta.url).href;
}

const contents = ref([
  {
    id: 1,
    img: "01",
    remark: "在線",
    title: "星達威鉑數位整合行銷",
    link: "https://starvibe.com.tw/",
    pc: "",
    web: "",
    text: "協助公司製作形象官網，使用 HTML、SCSS、jQuery 快速構建。",
    skills: ["SCSS", "HTML", "jQuery"],
  },
  {
    id: 2,
    img: "02",
    remark: "已下架(可查看網頁截圖)",
    title: "LOTTE XYLITOL x BTS 防彈少年團",
    link: "https://www.behance.net/gallery/184689285/_?",
    text: "製作方向為活動網站，使用 HTML、CSS、jQuery 快速構建，提供給與後端工程師，以便於將抽獎資料記錄到後台。",
    skills: ["CSS", "HTML", "jQuery", "AJAX"],
  },
  {
    id: 3,
    img: "03",
    remark: "已下架(經同意掛載)",
    title: "yuga 法國茶道活動網頁",
    link: "https://c3d1997.github.io/yuga/",
    text: "此網頁為接案製作，架構為活動網站，使用 HTML、CSS、jQuery 快速構建。",
    skills: ["SCSS", "HTML", "jQuery"],
  },
  {
    id: 4,
    img: "04",
    remark: "已下架(可查看網頁截圖)",
    title: "新光西瓜活動集點 Line 活動網頁",
    link: "https://www.behance.net/gallery/184733365/Line",
    text: "此網頁主要服務於 Line 應用程式內，客戶僅要求製作手機板型，內容較多數據紀錄性質，本專案主要負責切版以及彈出視窗呈現，並優化 UX 體驗。",
    skills: ["SCSS", "HTML", "jQuery"],
  },
  {
    id: 5,
    img: "05",
    remark: "在線",
    title: "外幣刷卡活動 - 滙豐(台灣) | 台灣",
    link: "https://shop.hsbc.com.tw/International/",
    text: "協助匯豐製作資訊網頁，使用 HTML、CSS、jQuery 快速構建。",
    skills: ["CSS", "HTML", "jQuery"],
  },
  {
    id: 6,
    img: "06",
    remark: "在線",
    title: "刷卡優惠 - 滙豐(台灣) | 台灣",
    link: "https://shop.hsbc.com.tw/",
    text: "協助匯豐製作資訊網頁，使用 HTML、CSS、jQuery 快速構建。",
    skills: ["CSS", "HTML", "jQuery"],
  },
  {
    id: 7,
    img: "07",
    remark: "已下架(可查看網頁截圖)",
    title: "摩根投資基金",
    link: "https://www.behance.net/gallery/184734613/_",
    text: "協助摩根投資基金製作一頁式資訊網頁，使用 HTML、SCSS、jQuery 快速構建。",
    skills: ["SCSS", "HTML", "jQuery"],
  },
  {
    id: 8,
    img: "08",
    remark: "已下架(可查看網頁截圖)",
    title: "摩根咖啡集點活動 Line 網頁",
    link: "https://www.behance.net/gallery/184735439/-LINE-",
    text: "協助摩根製作 Line 使用的集點網頁，使用 HTML、SCSS、jQuery 快速構建，並且有簡單使用 GSAP 製作動態。",
    skills: ["SCSS", "HTML", "jQuery", "GSAP"],
  },
  {
    id: 9,
    img: "09",
    remark: "已下架(可查看網頁截圖)",
    title: "紐崔萊1+1營養密技 Line 活動網頁",
    link: "https://www.behance.net/gallery/184735831/11",
    text: "協助紐崔萊製作 Line 使用的活動網頁，使用 HTML、SCSS、jQuery 快速構建，並且有簡單使用 GSAP 製作動態。",
    skills: ["SCSS", "HTML", "jQuery", "GSAP"],
  },
  {
    id: 10,
    img: "10",
    remark: "已下架(可查看網頁截圖)",
    title: "新光人壽60周年 Line 慶祝活動",
    link: "https://www.behance.net/gallery/184736229/60LINE",
    text: "協助新光人壽製作 Line 使用的活動網頁，使用 HTML、SCSS、jQuery、AJAX 快速構建，並且有簡單使用 GSAP 製作動態，但由於 api 已經關閉，無法獲取更多的網頁畫面。",
    skills: ["SCSS", "HTML", "jQuery", "GSAP", "AJAX"],
  },
  {
    id: 11,
    img: "",
    remark: "無法提供畫面",
    title: "凱基證卷共銷查詢系統",
    link: "",
    text: "協助凱基證卷製作後台操作系統，內容主要皆為數據傳出以及查找資料，我主要負責 UI/UX 設計並且進行畫面切版，並協助後端確認資料來源，過程非常有趣。",
    skills: ["SCSS", "HTML", "jQuery", "Bootstrap"],
  },
  {
    id: 12,
    img: "",
    remark: "無法提供畫面",
    title: "新光西瓜點數後台紀錄系統",
    link: "",
    text: "協助新光人壽製作後台活動查詢系統，內容主要為查看點數紀錄詳情以及中獎紀錄，我主要負責 UI/UX 設計並且進行畫面切版。",
    skills: ["SCSS", "HTML", "jQuery", "Bootstrap"],
  },
  {
    id: 13,
    img: "",
    remark: "無法提供畫面",
    title: "新光全國繪畫比賽後台",
    link: "",
    text: "協助新光人壽製作繪畫比賽後台操作系統，內容主要服務於繪畫比賽案件報名，查看報名紀錄，我主要負責 UI/UX 設計並且進行畫面切版。",
    skills: ["SCSS", "HTML", "jQuery", "Bootstrap"],
  },
]);
</script>
<style scoped>
.list {
  color: white;
  display: flex;
  flex-wrap: wrap;
  gap: 60px;
}
.listThing {
  width: 100%;
  overflow: hidden;
  border-radius: 20px 20px 0 0;
}
.listThing > p:nth-child(2) {
  line-height: 26px;
  font-weight: bold;
  display: inline;
}
.listThing > p:nth-child(4) {
  line-height: 26px;
  font-weight: normal;
  color: rgba(255, 255, 255, 0.747);
}
.remark {
  font-size: 12px;
  padding: 12px;
  color: rgba(255, 255, 255, 0.61);
}
.listThing > a {
  line-height: 26px;
  color: white;
  font-weight: bold;
}
.imgBox {
  width: 100%;
  overflow: hidden;
  max-height: 300px;
  margin-bottom: 16px;
}

.imgBox > img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.skill {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin: 10px 0 0 0;
}
.tag {
  display: block;
  border: 1px solid rgba(255, 255, 255, 0.4);
  color: rgba(255, 255, 255, 0.4);
  padding: 4px 10px;
  font-size: 12px;
}
@media screen and (max-width: 500px) {
  .imgBox {
    width: 100%;
    overflow: hidden;
    height: 600px;
  }
  .imgBox > img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .remark {
    display: block;
    padding: 0 0 12px 0;
  }
}
</style>