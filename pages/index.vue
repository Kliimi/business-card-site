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
      <img src="~/assets/images/photo_2022-03-30_13-11-00.jpg">
    </div>
  </main>
</template>

<script>

export default {
  name: 'IndexPage',
  layout: 'default-page',
  head: {
    title: 'Kliimi'
  }
}
</script>

<style scoped>
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
  width: 25vw;
  height: 25vw;
  border-radius: 50%;
  margin-top: 2em;
  margin-left: 4em ;
}
</style>
