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
        我是名熱情的跨領域轉職者，現在專注於前端開發領域，擁有一年的實務經驗。我的轉職之旅始於對技術的強烈興趣，這驅使我在利用業餘時間學習中迅速掌握了前端開發的核心技術，包括
        HTML、CSS 和
        JavaScript。我對高質量網站開發的專注不僅限於現有技術，目前正在積極自學
        Vue 框架並探索其他編程語言和框架，以豐富我的技術棧和視野。
      </p>
      <p>
        我對追踪前端開發的最新趨勢充滿熱情，並將這些知識運用於創建美觀且用戶友好的網站。在團隊合作中，我致力於追求卓越，並將從學習到實踐的每一步作為成長和進步的機會。我所做的每一步努力都源於對技術的熱愛和對於專業轉型的堅定決心，這驅動我在這個充滿挑戰與機會的領域不斷進取。
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