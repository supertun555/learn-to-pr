<template>
  <section class="container">
    <div align="center">
      <h1>Learn to PR</h1>
      <nuxt-link to="nuttakit">Nuttakit</nuxt-link>
      <h1>Plan Fitness</h1><br>
      <table border="1px solid black">
        <tr>
          <td>Sunday</td>
          <td>Monday</td>
          <td>Tuesday</td>
          <td>Wednesday</td>
          <td>Thursday</td>
          <td>Friday</td>
          <td>Saturday</td>
          <td>Delete</td>
        </tr>
        <tr v-for="(users, index) in user">
          <td><b>{{ users.suns }}</b></td>
          <td><b>{{ users.mons }}</b></td>
          <td><b>{{ users.tues }}</b></td>
          <td><b>{{ users.weds }}</b></td>
          <td><b>{{ users.thus }}</b></td>
          <td><b>{{ users.fris }}</b></td>
          <td><b>{{ users.sats }}</b></td>
          <td><button @click="deletePlan(index)">Delete</button></td>
        </tr>
        <tr>
          <td><b>{{isuns}}</b></td>
          <td><b>{{imons}}</b></td>
          <td><b>{{itues}}</b></td>
          <td><b>{{iweds}}</b></td>
          <td><b>{{ithus}}</b></td>
          <td><b>{{ifris}}</b></td>
          <td><b>{{isats}}</b></td>
          <td><button>delete</button></td>
        </tr>
        <tr>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="isuns"></td>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="imons"></td>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="itues"></td>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="iweds"></td>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="ithus"></td>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="ifris"></td>
          <td><input type="text" placeholder="ใส่ข้อมูล" v-model="isats"></td>
          <td><button @click="addUser">ok</button></td>
        </tr>
      </table>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      isuns: '',
      imons: '',
      itues: '',
      iweds: '',
      ithus: '',
      ifris: '',
      isats: '',
      user: [
        {
          suns: '1',
          mons: '2',
          tues: '3',
          weds: '4',
          thus: '5',
          fris: '6',
          sats: '7'
        },
        {
          suns: '21',
          mons: '22',
          tues: '23',
          weds: '24',
          thus: '25',
          fris: '26',
          sats: '27'
        }
      ]
    }
  },
  methods: {
    addPlan: function () {
      if (this.isuns === '' || this.imons === '' || this.itues === '' || this.iweds === '' || this.ithus === '' || this.ifris === '' || this.sats === '') {
        return
      }
      this.user.push({
        suns: this.isuns,
        mons: this.imons,
        tues: this.itues,
        weds: this.iweds,
        thus: this.ithus,
        fris: this.ifris,
        sats: this.isats
      })
    },
    deleteUser: function (index) {
      this.user.splice(index, 1)
    }
  },
  computed: {
    isun: function () {
      return this.isuns
    },
    imons: function () {
      return this.imons
    },
    itues: function () {
      return this.itues
    },
    iweds: function () {
      return this.iweds
    },
    ithus: function () {
      return this.ithus
    },
    ifris: function () {
      return this.ifris
    },
    isats: function () {
      return this.isats
    }
  }
}
</script>

<style>
  td {
    height: auto;width: 50px;
  }
</style>
