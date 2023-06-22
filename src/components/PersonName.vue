<script>
import FormUser from './FormUser.vue';

import PersonInfo from './PersonInfo.vue';
export default {
    data() {
        return {
            name: "Marcelo"
        };
    },
    components: { PersonInfo, FormUser }
}
</script>

<template>
  <div className="flex flex-col gap-8 items-center justify-center ">
    <div>
      <h2 class="text-purple-500 font-semibold">Esta é a descrição da pessoa {{ name }}</h2>
    </div>
    <div class="flex  gap-4">
      <PersonInfo />
      <PersonInfo />
    </div>
    <div>
      <h2 class="text-purple-500 font-semibold text-center mb-5">Adicione uma tecnologia</h2>  
      <FormUser/>
    </div>
  </div>
</template>
