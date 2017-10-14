<template>
  <div class='hello'>
    <br>
    <center>
      <h1>Rachata Page</h1> <br>
      <h2>Add</h2>
      <input type="text" name="" value="" v-model="newdata">
      <button type="button" name="button" @click="add" class="add">+</button><br><br>
      <h2>Search</h2><input type="text" name="" value="" v-model="search">
      <table >
        <tr style="text-align: left" v-for="d,index in filteredList">
          <td>{{d}}</td>
          <td><button type="button" name="button" class="del" @click="del(index)"> del </button></td>
        </tr>
      </table>
    </center>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  data () {
    return {
      data2: [
        'Rachata',
        'Fluk',
        'Tongpakdee',
        'Silawat',
        'Leelas',
        'Flame'
      ],
      newdata: '',
      search: ''
    }
  },
  methods: {
    add () {
      if (this.newdata === '') {
        return
      }
      this.data2.push(this.newdata)
      this.newdata = ''
    },
    del (i) {
      this.data2.splice(i, 1)
    }
  },
  computed: {
    filteredList () {
      return this.data2.filter(post => {
        return post.toLowerCase().includes(this.search.toLowerCase())
      })
    }
  }
}
</script>

<style scoped>
input[type=text] {
    width: 10%;
    -webkit-transition: width 0.4s ease-in-out;
    transition: width 0.4s ease-in-out;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid ##01DFD7;
    border-radius: 4px;
    box-sizing: border-box;

}

input[type=text]:focus {
    width: 20%;
    border: 3px solid ##01DFD7;
}
.add {
    width: 4%;
    background-color: #00FF00;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.add:hover {
    background-color: #04B431
}
.del {
    width: 4%;
    background-color: #FE2E64;
    color: white;
    padding: 4px 18px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
}

.del:hover {
    background-color: #B40431;
}
</style>
