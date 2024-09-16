<template>
  <div class="flex items-center justify-center min-h-screen bg-gray-100" v-if="!autorisation">
    <div class="bg-white p-8 rounded-lg shadow-lg max-w-sm w-full">
      <h2 class="text-2xl font-semibold text-center mb-6">Accéder à mon portfolio</h2>
      <form @submit.prevent="checkPassword">
        <div class="mb-4">
          <label for="password" class="block text-gray-700">Mot de passe</label>
          <input
            v-model="passwordInput"
            type="password"
            id="password"
            class="w-full p-2 border border-gray-300 rounded-lg mt-2"
            placeholder="Entrez le mot de passe"
          />
        </div>
        <button
          type="submit"
          class="w-full bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-lg"
        >
          Soumettre
        </button>
      </form>
      <p v-if="errorMessage" class="text-red-500 mt-4 text-center">{{ errorMessage }}</p>
    </div>
  </div>
  <div class="relative h-full w-full bg-black" v-else>
    <div
      class="absolute bottom-0 left-0 right-0 top-0 bg-[linear-gradient(to_right,#4f4f4f2e_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] bg-[size:50px_50px]"
    ></div>
    <div
      class="absolute left-0 right-0 top-[-10%] mt-32 z-0 h-[1000px] w-[1000px] rounded-full bg-[radial-gradient(circle_400px_at_50%_300px,#fbfbfb36,#000)]"
    ></div>
    <div class="flex flex-col items-center h-screen justify-center">
      <navbar class="absolute z-10 top-0 rounded-xl text-gray-50 mt-12" />
      <heroTexte></heroTexte>
    </div>
    <div
      class="h-screen w-full bg-black flex flex-col z-50 justify-center items-center"
    >
      <div class="h-1/3 w-5/6">
          <img src="../assets/images/photolio.png" class="w-auto h-full p-4 rounded-lg" />
      </div>
      <div class="h-1/3 w-5/6 flex justify-center">
          <img src="../assets/images/kaizen.png" class="w-auto p-4 h-full rounded-lg" />
      </div>
      <div class="h-1/3 w-5/6 flex justify-end">
        <img src="../assets/images/photolio.png" class="w-auto h-full p-4 rounded-lg" />
      </div>
    </div>
    <div
      class="h-screen w-full absolute z-30 flex justify-center items-center bg-black"
    >
      <div
        class="absolute inset-0 -z-10 h-full w-full items-center px-5 py-24 [background:radial-gradient(125%_125%_at_50%_10%,#000_60%,#63e_100%)]"
      ></div>
      <aboutMe class="z-50"></aboutMe>
      <parallaxParticles class="absolute z-10" />
    </div>
    <div class="h-screen w-full flex justify-center items-center"></div>
  </div>
</template>

<script setup>
const correctPassword = 'enzo' 
let passwordInput = ref('')
const errorMessage = ref('')
const autorisation = ref(false)
const checkPassword = () => {
  if (passwordInput.value === correctPassword) {
    autorisation.value = true
    errorMessage.value = 'Vous êtes connecté'
  } else {
    autorisation.value = false
          console.log('autorisation', autorisation.value)
    errorMessage.value = 'Mot de passe incorrect'
  }
}
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
  scroll-behavior: smooth;
}
</style>
