<template>
  <header>
    <div>
      <nuxt-link to="/" class="logo">
        Kliimi
      </nuxt-link>
    </div>
    <ul class="navigation">
      <li class="navigation__item">
        <nuxt-link to="/">
          Главная
        </nuxt-link>
      </li>
      <li class="navigation__item">
        <nuxt-link to="/about-me">
          Обо мне
        </nuxt-link>
      </li>
      <li class="navigation__item">
        <nuxt-link to="/contacts-page">
          Контакты
        </nuxt-link>
      </li>
    </ul>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5em 2em;
  background: #2D1436;
}
.logo {
  position: relative;
  font-size: 2em;
  font-weight: bolder;
}
.logo:hover {
  color:#EE0979;
}
.navigation {
  gap: 2em;
  font-size: 1.1em;
  margin-right: 1em;
}
.navigation__item {
  position: relative;
  transition: all .8s;
}
.navigation__item > a:hover {
  color: #EE0979;
}
.navigation__item:after{
  content: "";
  position: absolute;
  height: 4px;
  top: auto;
  right: 50%;
  bottom: -1em;
  left: 50%;
  background: linear-gradient(90deg, #EE0979 0%, #FF6A00 100%);
  transition: all .3s ease-out;
}
.navigation__item:hover::after {
  right: 0;
  left: 0;
}
.nuxt-link-exact-active {
  color: #EE0979;
}
.nuxt-link-exact-active:after {
  content: "";
  position: absolute;
  height: 4px;
  top: auto;
  left: 0;
  bottom: -1em;
  right: 0;
  background: linear-gradient(90deg, #EE0979 0%, #FF6A00 100%);
}
.logo::after {
  display: none;
}
</style>
