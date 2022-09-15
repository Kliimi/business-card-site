<template>
  <main>
    <h2>Обо мне</h2>
    <p>
      Приветствую! Меня зовут Климова Наталия.
      Я Junior frontend разработчик.
      Я занимаюсь изучением frontend разработки самостоятельно уже около 8 месяцев. За это время я получила самый главный навык и мой источник удовольствия - навык эффективно обучаться. За 8 месяцев обучения я изучила  HTML5, CSS3.
      Научилась верстать адаптивно, кроссбраузерно. Познакомиласть с препроцессором SASS.
      Могу сделать сборку проекта на WebPack.

      Сейчас глубоко изучаю Vue (версия 2) и Nuxt. Могу сделать валидацию форм на Vue с помощью библиотеки VeeValidate.
      Данный сайт-визитка написан на Nuxt.
    </p>
    <div class="codewars-container">
      <h3>Мой аккаунт на CodeWars: </h3>
      <a href="https://www.codewars.com/users/Kliimi"><img src="https://www.codewars.com/users/Kliimi/badges/large" alt="CodeWars bage"></a>
    </div>
    <h3>Мои навыки: </h3>
    <div class="cards-container">
      <ProgressBar
        v-for="card in cards"
        :key="card.name"
        :card="card"
      />
    </div>
    <div class="circle" />
  </main>
</template>

<script>
import ProgressBar from '~/components/progress-bar.vue'
export default {
  components: { ProgressBar },
  layout: 'default-page',
  data () {
    return {
      cards: [
        { name: 'HTML', progress: '90', color: 'rgba(231,72,234,1)' },
        { name: 'CSS', progress: '90', color: 'rgba(26,188,156,1)' },
        { name: 'JavaScript', progress: '80', color: 'rgba(188,26,99,1)' },
        { name: 'Vue', progress: '65', color: 'rgba(234,110,72,1)' },
        { name: 'Nuxt', progress: '50', color: 'rgba(75,26,188,1)' }
      ]
    }
  }
}
</script>

<style scoped>
main {
  flex-direction: column;
  align-items: center;
  gap: 2em;
  height: calc(100vh - 59px);
}
main > p {
  max-width: 60%;
  font-size: 1.1em;
}
.codewars-container {
  display: flex;
  align-items: center;
  gap: 1em;
}
.cards-container {
  display: flex;
  flex-wrap: wrap;
  gap: 2em
}
</style>
