<template>
  <section class="container">
    <div>
      <h1>{{name}}</h1>
        todoList <br>
				<table>
					<tr @v-for="(name, index) in data">
						<td key={index}>
							{{name.first}}
						</td>
						<td>
							{{name.last}}
						</td>
						<td>
							<button @click="deleteData(index)">Delete</button>
						</td>
					</tr>
					</table>
        ชื่อ : <input type="text" v-model="first"> นามสกุล : <input type="text" v-model="last"> <button @click="add()">เพิ่ม</button>
				<button @click="data = []">Clear</button>
  
		</div>
  </section>
</template>

<script>
export default {
  name: 'Rittiphon',
  data () {
    return {
      name: 'Rittiphon Phoarun',
      data: [],
      first: '',
      last: ''
    }
  },
  methods: {
    add () {
      this.data.push({
        first: this.first,
        last: this.last
      })
      this.first = ''
      this.last = ''
    },
    deleteData (index) {
      this.data.splice(index, 1)
    }
  }
}
</script>
<style>

</style>
