<template>
  <Header></Header>
  <div class="t-set">
    <transition name="fade" mode="out-in">
      <div v-if="currentComponent === '作品集 →'">
        <AboutMe></AboutMe>
        <Experenced></Experenced>
      </div>
      <Profile v-else-if="currentComponent === '經歷 ←'"></Profile>
    </transition>
  </div>

  <ChangeBtn @ChangeComponents="handleChangeComponent"></ChangeBtn>
</template>
<script setup>
import "./assets/reset.css";
import "./assets/globo.css";
import AboutMe from "./components/AboutMe.vue";
import Footer from "./components/Footer.vue";
import Profile from "./components/Profile.vue";
import Experenced from "./components/Experienced.vue";
import Header from "./components/Header.vue";
import ChangeBtn from "./components/ChangeBtn.vue";
import { ref } from "vue";

const currentComponent = ref("作品集 →");

function handleChangeComponent(e) {
  currentComponent.value = e;
}
</script>
<style >
.fade-enter-active,
.fade-leave-active {
  transition: 1s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateX(10px);
}
.t-set {
  overflow: hidden;
}
</style>