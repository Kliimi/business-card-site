<template>
  <div class="slider-thumb" />
</template>

<style lang="scss" scoped>
.slider-thumb {
  position: absolute;
  display: block;
  width: 50vw;
  height: 50vw;
  border-radius: 72% 47% 82% 35% / 45% 45% 80% 66%;
  will-change: border-radius, transform, opacity;
  animation: sliderShape 6s linear infinite;
  -webkit-animation: sliderShape 6s linear infinite;
  @include l {
    width: 60vw;
    height: 60vw;
  }
  @include md {
    width: 80vw;
    height: 80vw;
  }
  @include sm {
    width: 95vw;
    height: 95vw;
  }
}
.st-orange {
  background: linear-gradient(90deg,#e52e71,#ff8a00);

}
.st-violet {
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
