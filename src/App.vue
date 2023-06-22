<template>
  <body class="bg-slate-800 h-screen">   
    <FirstComponent/>
    <LifeCyclaVue/>
    <Pessoa/>
  </body>
</template>

<script>
import FirstComponent from './components/FirstComponent.vue';
import LifeCyclaVue from './components/LifeCycla.vue';
import Pessoa from './components/PersonName.vue';
export default {
  name: 'App',
  components: {
    FirstComponent,
    LifeCyclaVue,
    Pessoa    
  }
}
</script>