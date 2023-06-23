<template>
  <div class="text-center">
    <button @click="submit" class="bg-purple-600 hover:bg-purple-700 mt-5 text-white font-bold py-2 px-4 rounded-full shadow-lg" type="button">Enviar</button>
    <p class="mt-4 text-green-300" v-show="showMsg">{{ msg }}</p>
  </div>
</template>

<script>
export default {
  name: 'SubmitButton',
  data() {
    return {
      showMsg: false,
      msg: 'Criado'
    }
  },
  methods: {
    submit() {
      this.showMsg = !this.showMsg;
      setTimeout(() => {
        this.showMsg = false;
      }, 2000);
      this.$emit('submit');
    }
  }
}
</script>
