<template>
  <h1 class="text-center text-purple-400">{{ loading }}</h1>
</template>

<script>
export default {
  data() {
    return {
      loading: 'Loading',
      dots: ''
    }
  },
  created() {
    this.animateDots()
  },
  methods: {
    animateDots() {
      setTimeout(() => {
        this.dots += '.'
        this.loading = this.loading.replace('.', '')
        this.loading += this.dots

        if (this.dots.length < 4) {
          this.animateDots()
        } else {
          setTimeout(() => {
            this.loading = ''
          }, 1000)
        }
      }, 1000)
    }
  }
}
</script>
