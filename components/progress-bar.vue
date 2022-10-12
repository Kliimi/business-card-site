<!-- eslint-disable vue/no-parsing-error -->
<template>
  <div class="container">
    <div class="card">
      <div class="box">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70" />
            <circle cx="70" cy="70" r="70" :style="calcDashoffset" />
          </svg>
          <div class="num">
            <h2>{{ card.progress }}<span>%</span></h2>
          </div>
        </div>
        <h2 class="text">
          {{ card.name }}
        </h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['card'],
  computed: {
    calcDashoffset () {
      const styleObject = {
        stroke: this.card.color,
        strokeDashoffset: 440 - (440 * this.card.progress) / 100,
        transition: 'all 1s ease-in-out'
      }
      return styleObject
    }
  }

}
</script>

<style lang="scss" scoped>
.container .card {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 220px;
  height: 260px;
  text-align: center;
  border-radius: 30px;
  background: #1C0A22;
  transition: 0.5s;
}
.container .card:hover {
  box-shadow: 0 15px 35px rgba(0,0,0,.5);
  transform: translateY(-10px);
}
.percent {
  position: relative;
  width: 150px;
  height: 150px;
  border-radius: 50%;
  background: #1C0A22;
  box-shadow: inset 0 0 50px #000;
}
.percent .num {
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 150px;
  height: 150px;
  border-radius: 50%;
}
.percent .num h2 {
  font-size: 40px;
  font-weight: 700;
  color: #777;
  transition: 0.5s;
}
.card:hover .percent .num h2 {
  font-size: 60px;
  color: #fff;
}
.percent .num h2 span {
  font-size: 24px;
  color: #777;
  transition: 0.5s;
}
.card:hover .percent .num h2 span {
  color: #fff;
}
.text {
  position: relative;
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: #777;
  transition: 0.5s;
  margin-top: 20px;
}
.card:hover .text {
  color: #fff;
}
svg {
  position: relative;
  width: 150px;
  height: 150px;
}
svg circle {
  width: 100%;
  height: 100%;
  stroke: #42204E;
  stroke-linecap: round;
  stroke-width: 10;
  fill: none;
  transform: translate(5px,5px);
}
svg circle:nth-child(2) {
  stroke-dasharray: 440;
  stroke-dashoffset: 440;
  animation: animate_progress 1s ease-in-out forwards;
}

</style>
