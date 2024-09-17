<template>
    <div
      class="h-screen w-full flex  z-50 justify-center items-center my-32"
    >
      <div class="h-2/3 w-full perspective "
      id="project">
        <img
          src="../assets/images/photolio.png"
          class="w-2/3 h-full p-4 rounded-lg transform rotate-x-12 rotate-y-6 "
        />
      </div>
      <div class="w-auto m-8 rounded-xl h-2/3 bg-blue-100">
        <div class="p-8">
        <h1>Hello</h1>
        </div>
      </div>
    </div>
  </template>
  
  <script lang="ts" setup> 
  </script>
  
  <style scoped>
 
  #project {
    transform: rotateX(-30deg) rotateY(-335deg);
    transform-style: preserve-3d;
  }
  .perspective {
    perspective: 1000px;
  }
  </style>