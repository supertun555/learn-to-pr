<template>
  <section class="hello">
    <div>
      <h1>Calculator</h1><br ><br>
    <form>
        <table>
            <tr>
            <td height="200px" colspan="4">{{num1}} {{operater}} {{result}} {{num2}} {{sum}}</td>
            </tr>
            <tr>
                <td><button @click="clickNum(7)">7</button></td>
                <td><button @click="clickNum(8)">8</button></td>
                <td><button @click="clickNum(9)">9</button></td>
                <td><button class="symbol" @click="operate('*')">*</button></td>
            </tr>
            <tr>
                <td><button @click="clickNum(4)">4</button></td>
                <td><button @click="clickNum(5)">5</button></td>
                <td><button @click="clickNum(6)">6</button></td>
                <td><button class="symbol" @click="operate('-')">-</button></td>
            </tr>
            <tr>
                <td><button @click="clickNum(1)">1</button></td>
                <td><button @click="clickNum(2)">2</button></td>
                <td><button @click="clickNum(3)">3</button></td>
                <td><button class="symbol" @click="operate('+')">+</button></td>
            </tr>
            <tr>
                <td><button @click="clickNum(0)">0</button></td>
                <td><button class="symbol" @click="clear()">C</button></td>
                <td><button class="symbol" @click="summation()">=</button></td>
                <td><button class="symbol" @click="operate('/')">/</button></td>
            </tr>
        </table>
    </form>
    </div>    
  </section>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      result: '',
      num: '',
      operater: '',
      num1: '',
      num2: '',
      sum: '',
      temp: '',
      sumEvent: 0
    }
  }
//   methods: {
//     clickNum: function (num) {
//       this.result = this.result + num
//     //   this.sum = ''
//     },
//     operate: function (op) {
//       if (this.operater === '' && this.sumEvent === 0) {
//         this.num1 = this.result
//         this.num1 *= 1
//       } else if (this.num1 === '') {
//         this.sum = ''
//         this.num1 = this.temp
//         this.num1 *= 1
//       }
//       this.operater = op
//       this.result = ''
//     },
//     clear: function () {
//       this.num1 = ''
//       this.num2 = ''
//       this.result = ''
//       this.operater = ''
//       this.sum = ''
//       this.sumEvent = 0
//     },
//     summation: function () {
//       this.num2 = this.result
//       this.num2 *= 1
//       this.result = ''
//       this.sum = ''
//       if (this.operater === '+') {
//         this.sum += this.num1 + this.num2
//       } else if (this.operater === '-') {
//         this.sum += this.num1 - this.num2
//       } else if (this.operater === 'x') {
//         this.sum += this.num1 * this.num2
//       } else if (this.operater === '/') {
//         this.sum += this.num1 / this.num2
//       }
//       this.temp = this.sum * 1
//       this.operater = ''
//       this.num1 = ''
//       this.num2 = ''
//       this.sumEvent = 1
//     }
//   }
}
</script>

<style>
h1 {
    text-align: center;
    font-size: 40px;
    font-family: 'Passion One', cursive;
}
div {
    padding: 25px;
    margin: 10px;
    text-align: center;
}
button {
    background-color:#DFDFDF;
    border: none;
    color: black;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    font-family: 'Passion One', cursive;
}
.symbol{
    background-color:#ff8000;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    font-family: 'Passion One', cursive;
}
</style>
