<script setup lang="ts">
import imgUrl from '/squares.svg'
import triangleUrl from '/triangle.svg'
import circlesUrl from '/circles.svg'


</script>
<template>
  <main id="welcome-container">
    <div class="home-container">
      <div class="img-container">
        <img :src="imgUrl" alt="" />
        <img :src="triangleUrl" alt="" />
        <img :src="circlesUrl" alt="" />
      </div>
      <div class="landing-intro">
        <h1>Let&apos;s bring <br> your vision <br> to <span>life</span></h1>
      </div>
    </div>
  </main>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');
#welcome-container{
  height: 100vh;
 
}
.home-container{
  padding-top: 5rem;
  width: 100vw;
  display: flex;
  flex-wrap: wrap;
  flex-direction:column;
}
.img-container {
  display: flex;
  gap: 40px;
  width: 100%;
  justify-content: center;
  
}
img {
  height: 170px;
  width: auto;
  color: black;
}
.landing-intro{
  width: 100%;
  display: flex;
  justify-content: center;
  color: black;
  font-size: 95px;
  line-height: 1;
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  margin-top: 2rem;
  text-align: center;
}
.landing-intro span{
  color: #0097b2;
}

@media screen and (max-width: 2140px ) {
  #welcome-container {
    padding-top: 0;
  }
  .home-container{
    margin-top: 2rem;
  }
  img{
    height: 99px;
    width: auto;
  }
  .landing-intro{
    font-size: 60px;
  }
}
@media screen and (max-width: 668px) {
  .landing-intro{
    font-size: 40px;
  }
  .home-container{
    width: 100%;
  }
  img {
    height: 60px;
  }

}
@media screen and (max-width: 400px) {
  .home-container{
    padding-top:0;
  }
  .landing-intro{
    font-size: 30px;
  }
  img {
    height: 50px;
  }
  #welcome-container {
    height: 65vh;
  }
}
</style>