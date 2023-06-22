<template>
  <form action="" class="flex flex-col gap-5 ">
  <input-email/>
  <input-text/>
  <submit-button/>
  </form>
</template>

<script>
import InputEmail from './InputEmail.vue'
import InputText from './InputText.vue'
import SubmitButton from './SubmitButton.vue'
export default {
  components: { InputEmail, InputText, SubmitButton },
  name: 'FormUser',
}
</script>