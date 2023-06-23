<template>
  <div class="flex flex-col items-center justify-center bg-slate-400 text-lg p-2 border-2 border-purple-600 rounded-lg py-2 px-4 focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent">
    <p v-if="is_working">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul class="flex flex-col gap-4 mt-2 text-xl p-4">
      <li class="border-2 border-purple-600 rounded-lg p-2 text-center focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent cursor-pointer hover:text-blue-500 hover:border-blue-500" v-for="technology in technologies" :key="technology">{{ technology }}</li>
    </ul>
    <InputText @technology-added="addTechnology"/>
  </div>
</template>

<script>
import InputText from './InputText.vue';

export default {
  name: 'PersonInfo',
  components: {
    InputText
  },
  data() {
    return {
      technologies: ['Javascript', 'NodeJs', 'VueJs', 'Typescript', 'ReactJs'],
      is_working: false,
    }
  },
  methods: {
    addTechnology(technology) {
      this.technologies.push(technology);
    }
  }
};
</script>
