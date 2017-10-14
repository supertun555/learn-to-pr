<template>
  <section class="container">
    <center>
     <div class="ds">
        <br>
        <h1>{{ pass }}</h1>
        <br>
        <button class="button" @click="input(7)">7</button>&nbsp;
        <button class="button" @click="input(8)">8</button>&nbsp;
        <button class="button" @click="input(9)">9</button>&nbsp;
        <br><br>
        <button class="button" @click="input(4)">4</button>&nbsp;
        <button class="button" @click="input(5)">5</button>&nbsp;
        <button class="button" @click="input(6)">6</button>&nbsp;
        <br><br>
        <button class="button" @click="input(1)">1</button>&nbsp;
        <button class="button" @click="input(2)">2</button>&nbsp;
        <button class="button" @click="input(3)">3</button>&nbsp;
        <br><br>
        <button class="button" @click="reset()">reset</button>&nbsp;
        <button class="button" @click="input(0)">0</button>&nbsp;
        <button class="button" @click="checkP()">check</button>&nbsp;
        <br><br>
        <button class="button" @click="hint()">Hint</button>
     </div>
    </center>
  </section>
</template>

<script>
export default {
  data () {
    return {
      pass: 'Password',
      check: '',
      count: 0
    }
  },
  methods: {
    input (num) {
      this.count++
      if (this.pass === 'Password') { this.pass = '' }
      if (this.count < 5) {
        if (num === 1) {
          this.pass = this.pass + '*'
          this.check = this.check + '1'
        } else if (num === 2) {
          this.pass = this.pass + '*'
          this.check = this.check + '2'
        } else if (num === 3) {
          this.pass = this.pass + '*'
          this.check = this.check + '3'
        } else if (num === 4) {
          this.pass = this.pass + '*'
          this.check = this.check + '4'
        } else if (num === 5) {
          this.pass = this.pass + '*'
          this.check = this.check + '5'
        } else if (num === 6) {
          this.pass = this.pass + '*'
          this.check = this.check + '6'
        } else if (num === 7) {
          this.pass = this.pass + '*'
          this.check = this.check + '7'
        } else if (num === 8) {
          this.pass = this.pass + '*'
          this.check = this.check + '8'
        } else if (num === 9) {
          this.pass = this.pass + '*'
          this.check = this.check + '9'
        } else if (num === 0) {
          this.pass = this.pass + '*'
          this.check = this.check + '0'
        }
      } else {
        alert('Password has only 4 numbers!!')
      }
    },
    reset () {
      this.pass = 'Password'
      this.count = 0
      this.check = ''
    },
    checkP () {
      if (this.check === '2103') {
        alert('Login!!')
        window.location.href = 'https://www.facebook.com/'
      } else {
        alert('Wrong password!!')
      }
      this.pass = 'Password'
      this.count = 0
      this.check = ''
    },
    hint () {
      alert('Thailand president\' birthday/month !!')
    }
  }
}
</script>

<style>
.button {
   border: 1px solid #0a3c59;
   background: #3e779d;
   background: -webkit-gradient(linear, left top, left bottom, from(#65a9d7), to(#3e779d));
   background: -webkit-linear-gradient(top, #65a9d7, #3e779d);
   background: -moz-linear-gradient(top, #65a9d7, #3e779d);
   background: -ms-linear-gradient(top, #65a9d7, #3e779d);
   background: -o-linear-gradient(top, #65a9d7, #3e779d);
   background-image: -ms-linear-gradient(top, #65a9d7 0%, #3e779d 100%);
   padding: 10.5px 21px;
   -webkit-border-radius: 6px;
   -moz-border-radius: 6px;
   border-radius: 6px;
   -webkit-box-shadow: rgba(255,255,255,0.4) 0 1px 0, inset rgba(255,255,255,0.4) 0 1px 0;
   -moz-box-shadow: rgba(255,255,255,0.4) 0 1px 0, inset rgba(255,255,255,0.4) 0 1px 0;
   box-shadow: rgba(255,255,255,0.4) 0 1px 0, inset rgba(255,255,255,0.4) 0 1px 0;
   text-shadow: #7ea4bd 0 1px 0;
   color: gray;
   font-size: 14px;
   font-family: helvetica, serif;
   text-decoration: none;
   vertical-align: middle;
   }
.button:hover {
   border: 1px solid #0a3c59;
   text-shadow: #1e4158 0 1px 0;
   background: #3e779d;
   background: -webkit-gradient(linear, left top, left bottom, from(#65a9d7), to(#3e779d));
   background: -webkit-linear-gradient(top, #65a9d7, #3e779d);
   background: -moz-linear-gradient(top, #65a9d7, #3e779d);
   background: -ms-linear-gradient(top, #65a9d7, #3e779d);
   background: -o-linear-gradient(top, #65a9d7, #3e779d);
   background-image: -ms-linear-gradient(top, #65a9d7 0%, #3e779d 100%);
   color: #fff;
   }
.button:active {
   text-shadow: #1e4158 0 1px 0;
   border: 1px solid #0a3c59;
   background: #65a9d7;
   background: -webkit-gradient(linear, left top, left bottom, from(#3e779d), to(#3e779d));
   background: -webkit-linear-gradient(top, #3e779d, #65a9d7);
   background: -moz-linear-gradient(top, #3e779d, #65a9d7);
   background: -ms-linear-gradient(top, #3e779d, #65a9d7);
   background: -o-linear-gradient(top, #3e779d, #65a9d7);
   background-image: -ms-linear-gradient(top, #3e779d 0%, #65a9d7 100%);
   color: #fff;
   }

 .ds {
   background: gray;
   color: #fff;
   width: 300px;
   height: 350px;
 }
</style>
