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
        strokeDashoffset: 440 - (440 * this.card.progress) / 100
      }
      return styleObject
    }
  }

}
</script>

<style scoped>
.container .card
{
  position:relative;
  width:220px;
  background:#1C0A22;
  display:flex;
  justify-content:center;
  align-items:center;
  height:260px;
  border-radius: 30px;
  text-align:center;
  overflow:hidden;
  transition:0.5s;
}
.container .card:hover
{
  transform:translateY(-10px);
  box-shadow:0 15px 35px rgba(0,0,0,.5);
}
.percent
{
  position:relative;
  width:150px;
  height:150px;
  border-radius:50%;
  box-shadow: inset 0 0 50px #000;
  background:#1C0A22;
  z-index:1000;
}
.percent .num
{
  position:absolute;
  top:0;
  left:0;
  width:150px;
  height:150px;
  display:flex;
  justify-content:center;
  align-items:center;
  border-radius:50%;
}
.percent .num h2
{
  color:#777;
  font-weight:700;
  font-size:40px;
  transition:0.5s;
}
.card:hover .percent .num h2
{
  color:#fff;
  font-size:60px;
}
.percent .num h2 span
{
  color:#777;
  font-size:24px;
  transition:0.5s;
}
.card:hover .percent .num h2 span
{
  color:#fff;
}
.text
{
  position:relative;
  color:#777;
  margin-top:20px;
  font-weight:700;
  font-size:18px;
  letter-spacing:1px;
  text-transform:uppercase;
  transition:0.5s;
}
.card:hover .text
{
  color:#fff;
}
svg
{
  position:relative;
  width:150px;
  height:150px;
  z-index:10;
}
svg circle
{
  width:100%;
  height:100%;
  fill:none;
  stroke:#42204E;
  stroke-width:10;
  stroke-linecap:round;
  transform:translate(5px,5px);
}
svg circle:nth-child(2)
{
  stroke-dasharray:440;
  stroke-dashoffset:440;
}

</style>
