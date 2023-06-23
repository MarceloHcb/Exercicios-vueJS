<template>
<img class="rounded-full w-11" :src="avatar" :alt="descricao">
</template>

<script>
export default {
  name: 'Picture_avatar',
  data()  {
    return {
      avatar: "https://avatars.githubusercontent.com/u/50005589?v=4",
      descricao:"Foto do avatar"
    }
  }
}
</script>