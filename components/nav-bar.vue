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

<style lang="scss" scoped>
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
  top: auto;
  bottom: -1em;
  left: 50%;
  right: 50%;
  height: 4px;
  background: linear-gradient(90deg, #EE0979 0%, #FF6A00 100%);
  transition: all .3s ease-out;
}
.navigation__item:hover::after {
  left: 0;
  right: 0;
}
.nuxt-link-exact-active {
  color: #EE0979;
}
.nuxt-link-exact-active:after {
  content: "";
  position: absolute;
  top: auto;
  bottom: -1em;
  left: 50%;
  right: 50%;
  height: 4px;
  background: linear-gradient(90deg, #EE0979 0%, #FF6A00 100%);
}
.logo::after {
  display: none;
}

</style>
