<template>
  <main>
    <div class="slider-thumb"></div>
    <div class="container">
      <h2>Связаться со мной:</h2>
      <ul>
        <li><span>Телефон:</span> <a href="tel:+7 996 634 86 90">+7 996 634 86 90</a></li>
        <li><span>E-mail:</span> <a href="mailto:natalykliimi@gmail.com">natalykliimi@gmail.com</a></li>
        <li><span>Telegram:</span> <a href="https://t.me/Kliimi">@Kliimi</a></li>
        <li><span>Github:</span> <a href="https://github.com/Kliimi">@Kliimi</a></li>
      </ul>
  </div>
  </main>
</template>

<script>
export default {
  layout: 'default-page'
}
</script>

<style scoped>
main {
  flex-direction: column;
  align-items: center;
  height: calc(100vh - 59px);
  overflow: hidden;
}
.container {
  position: relative;
  top: 10%;
}
.container > ul {
  flex-direction: column;
  gap: 1em;
  font-size: 1.2em;
}
.container ul li > span {
  font-weight: bolder;
}

.slider-thumb {
  position: absolute;
  display: block;
  width: 550px;
  height: 550px;
  border-radius: 72% 47% 82% 35% / 45% 45% 80% 66%;
  background: linear-gradient(90deg,#e52e71,#ff8a00);
  will-change: border-radius, transform, opacity;
  animation: sliderShape 6s linear infinite;
  -webkit-animation: sliderShape 6s linear infinite;
}
.slider-thumb:hover {
  background: linear-gradient(45deg, rgba(231,72,234,1) 0%, rgba(75,26,188,1) 100%);
}
@keyframes sliderShape{
  0%,100%{

    border-radius: 42% 58% 70% 30% / 45% 45% 55% 55%;
    transform: translate3d(0,0,0) rotateZ(0.01deg);
  }
  34%{
    border-radius: 70% 30% 46% 54% / 30% 29% 71% 70%;
    transform:  translate3d(0,5px,0) rotateZ(0.01deg);
  }
  50%{
    transform: translate3d(0,0,0) rotateZ(0.01deg);
  }
  67%{
    border-radius: 100% 60% 60% 100% / 100% 100% 60% 60% ;
    transform: translate3d(0,-3px,0) rotateZ(0.01deg);
  }
}

</style>
