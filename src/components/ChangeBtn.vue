<template>
  <div class="fixed">
    <button @click="ClickBtn">{{ BtnText }}</button>
  </div>
</template>
<script setup>
import { ref, defineEmits } from "vue";

const BtnText = ref("作品集 →");
const emit = defineEmits(["ChangeComponents"]);
function ClickBtn() {
  BtnText.value = BtnText.value === "作品集 →" ? "經歷 ←" : "作品集 →";
  emit("ChangeComponents", BtnText.value);
  // 如果按鈕文本是“經歷 ←”，則滾動到作品集部分
  setTimeout(function () {
    document.getElementById("headerTop").scrollIntoView({ behavior: "smooth" });
  }, 1000);
}
</script>
<style scoped>
.fixed {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #1e1e1e;
}
button {
  display: block;
  font-size: 20px;
  color: white;
  font-weight: 800;
  border: 1px solid white;
  padding: 6px 16px 6px 20px;
  line-height: 30px;
  margin: 30px auto;
}
button:hover {
  background-color: white;
  color: black;
  transition: 0.5s;
}
</style>