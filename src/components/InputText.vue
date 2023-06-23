<template>
  <div>
    <input type="text" placeholder="Tecnologia" v-model="technology" class="border-2 border-purple-600 rounded-lg py-2 px-4 focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" />
    <SubmitButton @submit="addTechnology" />
  </div>
</template>

<script>
import SubmitButton from './SubmitButton.vue';

export default {
  name: 'InputText',
  components: {
    SubmitButton
  },
  data() {
    return {
      technology: ''
    }
  },
  methods: {
    addTechnology() {
      this.$emit('technology-added', this.technology);
      this.technology = '';
    }
  }
}
</script>
