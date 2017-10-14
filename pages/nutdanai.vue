<template>
<div class="box" style="border: 1px solid blue;">
  <h3 class="title">ร้านอาหารตามสั่ง</h3>
  อาหารธรรมดา<p>
  <progress class="progress is=info" max="10" :value="counter"></progress>
  <p class="control">
    <button @click="increment(counter)" class="button">Buy</button>
    <h2>สามารถซื้อได้อีก {{ (10 - counter) }}</h2>
    <h2>ราคารวม {{ sum = counter*40 }}</h2>
  </p>
  <hr>


  อาหารพิเศษ<p>
  <progress class="progress is=info" max="10" :value="counter1"></progress>
  <p class="control">
    <button @click="incrementplus(counter1)" class="button">Buy</button>
    <h2>สามารถซื้อได้อีก {{ (10 - counter1) }}</h2>
    <h2>ราคารวม {{ sumplus = counter1*50 }}</h2>
  </p>
  <hr>

  ไข่ดาว<p>
  <progress class="progress is=info" max="10" :value="star"></progress>
  <p class="control">
    <button @click="incrementstar(star)" class="button">Buy</button>
    <h2>สามารถซื้อได้อีก {{ (10 - star) }}</h2>
    <h2>ราคารวม {{ sumstar = star*10 }}</h2>
  </p>
  <hr>

  รายการอาหาร<p>
    อาหารธรรมดา X {{counter}} <p>
    อาหารพิเศษ X {{counter1}} <p>
    ไข่ดาว X {{star}} <p>
  <p class="control">

    <h2>ราคารวม {{ sum+sumplus+sumstar }}</h2>
  </p>
  <hr>



</div>
</template>
<script>
export default {
  data () {
    return {
      counter: 0,
      counter1: 0,
      star: 0
    }
  },
  methods: {
    increment (counter) {
      if (counter <= 9) {
        this.counter += 1
        return this.counter
      }
    },
    incrementplus (counter1) {
      if (counter1 <= 9) {
        this.counter1 += 1
        return this.counter1
      }
    },
    incrementstar (star) {
      if (star <= 9) {
        this.star += 1
        return this.star
      }
    }
  },
  components: {
  }
}
</script>
