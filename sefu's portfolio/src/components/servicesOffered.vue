<script setup lang="ts">
import webdevUrl from '/builder.svg'
import webDesign from '/design.svg'
import webMain from '/maintenance.svg'
import 'primeicons/primeicons.css'

import Button from 'primevue/button';
</script>
<template>
  <main class="main-container">
    <div class="title-container">
      <p id="title">Services Offered</p>
    </div>
    <div class="service-container">
      <div id="web-container">
        <img :src="webdevUrl" alt="" />
        <span>Web Development</span>
        <p>
          Covering front-end and back-end development, including website creation, customization,
          and optimization.
        </p>
      </div>
      <div id="webD-container">
        <img :src="webDesign" alt="" />
        <span>Web Design</span>
        <p>
          Providing UI/UX design services to enhance user experience and create visually appealing
          websites.
        </p>
      </div>
      <div id="web-maintenance">
        <img :src="webMain" alt="" />
        <span>Website Maintenance</span>
        <p>
          Offering ongoing support, updates, and troubleshooting to ensure your website remains
          functional and up-to-date.
        </p>
      </div>
    </div>
    <div id="button-container">
      <Button label="Explore My Works"  class="p-button-raised p-button-secondary" id="projects-button"/>
    </div>
  </main>
</template>
<style>
.main-container{
  height: 100vh;
  width: 100vw;
}
.service-container {
  padding-top: 5rem;
  width: 100%;
  height: 70vh;
  display: flex;
  flex-direction: row;
  justify-content: center;
  text-align: center;
  gap: 10rem;
}

.service-container img {
  width: 15rem;
  height: auto;
  margin: auto;
  padding-bottom: 2rem;
}
.service-container span {
  font-size: 35px;
  font-weight: 900;
  color: #0097b2;
}
.service-container p {
  font-size: 25px;
}
#web-container{
  width: 25rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 15rem;
  height: 50vh;
}
#webD-container{
  width: 25rem;
  display: flex;
  flex-direction: column;
  height: 40vh;
}
#web-maintenance{
  width: 25rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 15rem;
  height: 50vh;
}

#button-container{
  width: 100%;
  display: flex;
  justify-content: center;

}
#projects-button{
  width:15rem;
  height: 3rem;
  font-size: 20px;
  font-family: "Roboto", sans-serif;
  font-weight: 100;
  background-color: white;
  color: black;
  border-radius: 10px;
}

/* smaller screen */
@media (max-width: 1665px) {
  
  .service-container img {
    width: 10rem;
  }
  .service-container span {
    font-size: 25px;
  }
  .service-container p {
  font-size: 20px;
}
}
@media screen and (max-width: 1500px ) {
  .service-container{
    flex-direction: column;
    height: 120vh;
    gap: 5rem;
    padding-top: 8rem;
    align-items: center
  }
  #web-maintenance, #webD-container, #web-container {
   padding-top: 0;
   height: auto;
   width: 60%;
}
.service-container img {
    width: 15rem;
  }
  .service-container span {
    font-size: 35px;
  }
  .service-container p {
  font-size: 25px;
}
#button-container{
  padding: 5rem;
}
}
@media screen and (max-width: 730px) {
  #web-maintenance, #webD-container, #web-container {
   width: 100%;
   align-items: center;
}
  .service-container img {
    width: 8rem;
  }
  .service-container span {
    font-size: 25px;
  }
  .service-container p {
  font-size: 18px;
  width: 90%;
}
.service-container{
  height: 180vh;
  padding: 0%;
}
#button-container{
  padding-bottom: 5rem;
  padding-top: 0;
}
}
</style>
