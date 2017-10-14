<template>
  <section class="container">
    <center><div>
      <h1>ปุ่มกดเลข หรรษา</h1><br>
      <button type="text"   id="show" class="t" @click="show" :value="cal"></button><br>
      <button type="button" id="one"  class="p" @click="one">1</button>
      <button type="button" id="two" class="p" @click="two">2</button>
      <button type="button" id="three"  class="p" @click="three">3</button><br>
      <button type="button" id="four"  class="p" @click="four">4</button>
      <button type="button" id="five"  class="p" @click="five">5</button>
      <button type="button" id="six"  class="p" @click="six">6</button><br>
      <button type="button" id="seven"  class="p" @click="seven">7</button>
      <button type="button" id="eight"  class="p" @click="eight">8</button>
      <button type="button" id="nine"  class="p" @click="nine">9</button><br>
      <button type="button" id="zero"  class="p" @click="zero">0</button>
      <button type="button" id="plus"  class="p" @click="plus">+</button>
      <button type="button" id="del"  class="p" @click="del">-</button><br>
      <button type="button" id="multiply"  class="p" @click="multiply">*</button>
      <button type="button" id="divide" class="p" @click="divide">/</button>
      <button type="button" id="as"  class="p" @click="as">=</button><br>
      <button type="button" id="clear"  class="t" @click="clear">C</button>
    </div></center>
  </section>
</template>
<script>

</script>


<style>
.p {
 width : 60px ;
 height : 60px ;
}
.t {
 width : 180px ;
 height : 60px ;
}
</style>

<script>
export default {

  components: {
  },

  data () {
    return {
    }
  },

  methods: {
  }
}
</script>
