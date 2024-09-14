<template>
  <div class="relative h-full w-full bg-black">
    <div
      class="absolute bottom-0 left-0 right-0 top-0 bg-[linear-gradient(to_right,#4f4f4f2e_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] bg-[size:50px_50px]"
    ></div>
    <div
      class="absolute left-0 right-0 top-[-10%] mt-32 z-0 h-[1000px] w-[1000px] rounded-full bg-[radial-gradient(circle_400px_at_50%_300px,#fbfbfb36,#000)]"
    ></div>
    <div class="flex flex-col items-center h-screen justify-center">
        <navbar class="absolute z-10 top-0 rounded-xl text-gray-50 mt-12"/>
      <heroTexte></heroTexte>
    </div>
    <div class="h-screen w-full absolute z-30 flex justify-center items-center bg-black">
        <aboutMe></aboutMe>
    </div>
  </div>
</template>

<script lang="ts">
</script>

<style lang="css">
@import url("https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,200..800&display=swap");
.brico-800 {
  font-family: "Bricolage Grotesque", sans-serif;
  font-optical-sizing: auto;
  font-weight: 800;
  font-style: normal;
  font-variation-settings: "wdth" 100;
}
.brico-200 {
  font-family: "Bricolage Grotesque", sans-serif;
  font-optical-sizing: auto;
  font-weight: 200;
  font-style: normal;
  font-variation-settings: "wdth" 100;
}

* {
  padding: 0;
  margin: 0;
}
</style>
