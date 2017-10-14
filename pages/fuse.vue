<template>
  <section class="container">
      <center>
      <h2>Wellcome to proflie</h2>
      <h1>Fuse</h1><br><br>
      <button @click="proflie()">Click on</button>
      <div id="myDIV">
        Peerapon
      </div>
    </center>
  </section>
</template>

<script>
export default {
  components: {
  },
  methods: {
    proflie () {
      console.log('asdasda')
      var x = document.getElementById('myDIV')
      if (x.style.display === 'none') {
        x.style.display = 'block'
      } else {
        x.style.display = 'none'
      }
    }
  }
}
</script>

<style>
    button {
        background-color: black; /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    }
</style>
