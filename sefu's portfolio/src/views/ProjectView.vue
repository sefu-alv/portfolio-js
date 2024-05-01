<script setup lang="ts">

</script>

<template>
    <div class="projects-section">
      <div id="title-container">
        <span>My works</span>
        <p>
          This section is filled with my works. Clicking on a project will take you to a page describe
          the project, technologies used, and its challenges
        </p>
      </div>
      <div class="projects-container">
        <div id="projects-scroll">
          <div class="card">
            <h2>Card 1</h2>
            <p>This is the content of card 1.</p>
          </div>
          <div class="card">
            <h2>Card 2</h2>
            <p>This is the content of card 2.</p>
          </div>
          <div class="card">
            <h2>Card 3</h2>
            <p>This is the content of card 3.</p>
          </div>
          <div class="card">
            <h2>Card 4</h2>
            <p>This is the content of card 4.</p>
          </div>
          <div class="card">
            <h2>Card 5</h2>
            <p>This is the content of card 5.</p>
          </div>
          <div class="card">
            <h2>Card 6</h2>
            <p>This is the content of card 6.</p>
          </div>
          <div class="card">
            <h2>Card 7</h2>
            <p>This is the content of card 7.</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <style>
    .card {
      height: 35vh;
      padding: 20px;
      margin: 10px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      background-color: #ffffff;
      text-align: center;
    }
      
    .card h2 {
      margin-top: 0;
    }
      
    .card p {
      margin-bottom: 0;
    }
  
    .projects-section {
      display: flex;
      justify-content: center;
      flex-direction: column;
    }
  
    #title-container {
      padding-top: 90px;
      width: 100%;
      height: 50vh;
      text-align: center;
    }
  
    #title-container span {
      font-size: 70px;
      font-weight: 500;
    }
  
    #title-container p {
      font-weight: lighter;
      font-size: 20px;
    }
  
    .projects-container {
      width: 100%;
      height: 50vh;
    }
  
    #projects-scroll {
      display: grid;
      grid-auto-flow: column;
      grid-auto-columns: 25%;
      overflow-x: auto; /* Enable horizontal scrolling */
      overscroll-behavior-inline: contain;
    }
  
    @media screen and (max-width: 500px) {
      #projects-scroll {
        grid-auto-columns: 100%;
      }
    }
  </style>
  