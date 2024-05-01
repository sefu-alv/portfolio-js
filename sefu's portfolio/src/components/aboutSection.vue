<script setup lang="ts">
import downloadURL from '/download.svg'
import { ref, onMounted } from 'vue'

const intro = "Who am I?";
const typedText = ref("");
let index = 0;

function typeText() {
  if (index < intro.length) {
    typedText.value += intro.charAt(index);
    index++;
    setTimeout(typeText, 70);
  }
}

onMounted(typeText);

</script>
<template>
  <div class="about">
    <div class="title-container">
      <p id="title">{{ typedText }}</p>
    </div>
    <div class="about-container">
      <div class="about-text">
        <p>
          I'm a <span>full-stack</span> web developer excited 
          to turn your ideas into functional 
          websites. From design to implementation, 
          I'm here to make your online vision a reality
        </p>
        <div class="button-container">
          <button id="resume">Resume <img :src="downloadURL" alt="" /></button>
        </div>
      </div>
      <div class="pfp">
        <img src="https://placehold.co/300x500" alt="" />
      </div>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');

.about {
  width: 100vw;
  min-height: 100vh;
}
.about-container {
  width: auto;
  height: 65vh;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
}
.about-text {
  width: 50%;
  color: black;
  font-family: 'Roboto', sans-serif;
  font-size: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.about-text span {
  color: #0097b2;
}
.about-text p {
  width: 60%;
}
#resume {
  font-size: 20px;
  width: 150px;
  height: 50px;
  border-radius: 20px;
  background-color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 4px;
}
.button-container {
  display: flex;
  width: 60%;
  margin-top: 2rem;
}
button img {
  width: 20px;
  height: 20px;
}
.pfp {
  width: 50%;
  height: 60vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title-container{
  width: 100%;
  display: flex;
  justify-content: center;
  
}
#title{
  font-size: 70px;
  font-family: "Roboto" sans-serif;
  font-weight: 700;
}
@media screen and (max-width: 2140px) {
  .about-text p{
    width: 80%;
    padding-left: 5rem;
  }
  .button-container{
    width: 80%;
    padding-left: 5rem;
  }
 
}
@media screen and (max-width: 2050px) {
  .about-text{
    font-size: 35px;
  }
}
@media screen and (max-width: 1500px) {
  .about-text{
    font-size: 30px;
  }
}
@media screen and (max-width: 1050px) {
  .about-container{
    flex-direction: column-reverse;
    height: 110vh;

  }
  .pfp {
    width: 90%;
    height: 30vh;
  }
  .about-text{
    width: 90%;
  }
}
@media screen and (max-width: 500px) {
  .about-container{
    height: auto;
  }
  .pfp {
    width: 95%;
    height: 20vh;
  }
  .about-text{
    width: 100%;
    font-size:15px;
    padding: 0;
  }
  .about-text p {
  width: 85%;
  padding: 0;
  text-align: center;
  
}

#title{
  font-size: 40px;
}
.button-container{
  padding: 0;
  justify-content: center;
  width: 30%;
  height: auto;
}
}
</style>
