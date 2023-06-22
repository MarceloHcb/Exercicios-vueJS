<template>
  <div class="flex flex-col gap-4  items-center justify-center text-purple-500">
    <h1>Olá Vue</h1>
    <p>Meu nome é {{ name }}</p>
    <p>Estou iniciando o curso de {{ curso }}</p>
  </div>
  </template>

<script>
export default {
  name: 'FirstComponent',
  data()  {
    return {
      name: "Marcelo",
      curso:"Vue.js"
    }
  }
}
</script>