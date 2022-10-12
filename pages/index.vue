<template>
  <main>
    <LightsBackground />
    <div class="container">
      <div>
        <h1>Добро пожаловать!</h1>
        <h3>Меня зовут Наталия Климова</h3>
        <h3>Я junior frontend разработчик</h3>
        <ul>
          <li>
            <NuxtLink to="/about-me" class="button b-red rot-135">
              Немного информации обо мне
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/contacts-page" class="button b-red rot-135">
              Связаться со мной
            </NuxtLink>
          </li>
        </ul>
      </div>
      <img src="~/assets/images/photo_2022-09-19_16-46-46.jpg">
    </div>
  </main>
</template>

<script>

export default {
  name: 'IndexPage',
  head: {
    title: 'Kliimi'
  }
}
</script>

<style lang="scss" scoped>
main {
  padding-top: 0;
  justify-content: center;
}
.container {
  position: absolute;
  top: 20%;
  display: flex;
  text-align: center;
  justify-content: space-evenly;
  @include md {
    flex-direction: column;
    top: 8%;
    h1 {
      font-size: 2.4em;
      margin-bottom: 1.1em;
    }
  }
}

ul {
  flex-direction: column;
  align-items: center;
  gap: 1.5em;
  margin-top: 4em;
}
li {
  padding: 1em;
}
img {
  max-width: 25vw;
  max-height: 25vw;
  border-radius: 50%;
  margin-top: 2em;
  margin-left: 4em ;
  @include md {
    max-width: 85vw;
    max-height: 85vw;
    margin: 2em auto 0;
  }
}
</style>
