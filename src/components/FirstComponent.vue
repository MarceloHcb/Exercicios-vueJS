<template>
  <div class="flex flex-col gap-4 items-center justify-center text-purple-500">
    <h1>Olá Vue</h1>
    <p>Meu nome é {{ name }}</p>
    <p>Estou iniciando o curso de {{ curso }}</p>
    <p>Para acessar meu portifólio <a class="cursor-pointer" v-bind:href="meu_link" target="_blank">Clique Aqui!</a></p>
    <PictureAvatar/>
  </div>
</template>

<script>
import PictureAvatar from './Picture_avatar.vue'

export default {  
  name: 'FirstComponent',
  components: {
    PictureAvatar
  },
  data() {
    return {
      name: "Marcelo",
      curso: "Vue.js",
      meu_link: "https://google.com"
    }
  }
}
</script>
