<template>
  <div class="hello"><br>
    <center><h1>ร้านอาหารตามสั่ง</h1><br><br>
    <button style="border-radius: 8px;background-color:#CCFFCC;" @click="addMenu('ธรรมดา',30)"><h1>ธรรมดา 30</h1></button>&nbsp;&nbsp;
    <button  style="border-radius: 8px;background-color:#CCFFCC;" @click="addMenu('ทะเล',40)"><h1>ทะเล 40</h1></button> <br><br>
    <button style="border-radius: 8px;background-color:#CCFFCC;" @click="addMenu('ไข่ดาว',5)"><h1>ไข่ดาว 5</h1></button>&nbsp;&nbsp;&nbsp;&nbsp;
      <button style="border-radius: 8px;background-color:#CCFFCC;" @click="addMenu('ไข่เจียว',7)"><h1>ไข่เจียว 7</h1></button> <br><br>
    <button style="border-radius: 8px;background-color:#CCFFCC;" @click="addMenu('น้ำเปล่า',12)"><h1>น้ำเปล่า 12</h1></button>&nbsp;&nbsp;
      <button style="border-radius: 8px;background-color:#CCFFCC;" @click="addMenu('น้ำแข็ง',2)"><h1>น้ำแข็ง 2</h1></button> <br><br><hr>

    <table align="center">
      <tr>
        <td colspan="3"><button style="border-radius: 8px;background-color:#FFFF66;" @click="clear()"><h1>Clear</h1></button></td>
      </tr>
      <tr>
        <td colspan="3"><h1>ราคารวม {{costCount}} บาท</h1></td>
      </tr>
      <tr>
        <td>รายการ</td>
        <td>ราคา</td>
        <td></td>
      </tr>
      <tr>
        <td colspan="3"><hr></td>
      </tr>
      <tr v-for="(user, index) in users">
        <td>{{ user.name }}</td>
        <td>{{ user.cost }}</td>
        <td><button @click="deleteUser(index, user.cost)">Delete</button></td>
      </tr>
    </table></center>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      cost: 0,
      costCount: 0,
      users: [
      ]
    }
  },
  methods: {
    addMenu: function (nameM, costM) {
      this.users.push({
        name: nameM,
        cost: costM
      })
      this.costCount += costM * 1
    },
    deleteUser: function (index, cost) {
      this.costCount -= cost
      this.users.splice(index, 1)
    },
    clear: function () {
      this.users.splice(0, this.users.length)
      this.costCount = 0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
