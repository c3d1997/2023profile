<template>
  <Container :width="600" :mg-bottom="30">
    <div class="introduce">
      <img class="avatar" src="../assets/lc.png" alt="" />
      <div class="content">
        <h2>李承熹</h2>
        <p>前端工程師</p>
        <span>Front-end developer</span>
      </div>
    </div>
    <div class="aboutMe">
      <h3>關於我</h3>
      <p>
        我是一名具有一年職業經驗的前端開發者，過去的一年裡積累了寶貴的行業經驗，專注於高質量的網站開發。我能夠熟練運用
        HTML、CSS 和 JavaScript，並且正在自學 Vue
        框架相關應用，以提升我的技術棧。我熱衷於追踪前端開發的最新趨勢，並將這些知識應用於創建美觀、用戶友好的網站。在團隊合作中，我始終致力於實現卓越，並尋求不斷進步。
      </p>
    </div>
    <div class="aboutMe">
      <h3>聯絡資訊</h3>
      <div class="info">
        <p>郵件</p>
        <p>c3d1997@gmial.com</p>
      </div>
      <div class="info">
        <p>手機</p>
        <p>0976-150-619</p>
      </div>
      <div class="info">
        <p>Github</p>
        <a href="https://github.com/c3d1997">@c3d1997</a>
      </div>
    </div>
  </Container>
</template>
<script setup>
import Container from "./Container.vue";
</script>
<style scoped>
.introduce {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
}
.avatar {
  background-color: white;
  border-radius: 50%;
  width: 100px;
}
.content,
.aboutMe {
  color: white;
}
.info {
  display: flex;
}
.info p {
  line-height: 30px;
}
.info a {
  color: white;
}
.info > p:first-child {
  width: 100px;
  color: rgba(255, 255, 255, 0.514);
}
.content > span {
  font-size: 14px;
  color: gray;
}
.aboutMe {
  margin-top: 30px;
  line-height: 24px;
}
.aboutMe > h3 {
  text-align: center;
  margin-top: 40px;
  margin-bottom: 16px;
}
.aboutMe > p {
  text-align: justify;
}
</style>