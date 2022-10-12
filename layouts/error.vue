<template>
  <main class="__nuxt-error-page">
    <AnimateCircle class="st-violet" />
    <div class="container">
      <h1>{{ error.statusCode }}</h1>
      <h3>Вы заблудились. Но не беспокойтесь: вот правильный путь</h3>
      <nuxt-link to="/" class="button b-green rot-135">
        На Главную
      </nuxt-link>
    </div>
  </main>
</template>

<script>
export default {
  name: 'ErrorPage',
  layout: 'default-page',
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  head () {
    return {
      title: this.message,
      meta: [
        {
          name: 'viewport',
          content: 'width=device-width,initial-scale=1.0,minimum-scale=1.0'
        }
      ]
    }
  },
  computed: {
    statusCode () {
      return (this.error && this.error.statusCode) || 500
    },
    message () {
      return this.error.message
    }
  }
}

</script>

<style scoped>
main {
  justify-content: center;
}
.container {
  position: relative;
  text-align: center;
}
.container > h1 {
  font-size: 11em;
  margin: 0.2em auto;
}
.container > h3 {
  max-width: 90%;
  margin: 0 auto;
  margin-bottom: 3em;
}
</style>
