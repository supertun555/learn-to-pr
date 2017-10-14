<template>
  <section class="container">
  <center>  <div class='program'>
    <hr><h1>Game X O</h1><br><hr>
    <h1 v-if='msg%2===0'>{{ turn='X' }}</h1>
    <h1 v-else>{{ turn='O' }}</h1>
    <h2>Round : {{ msg }}</h2><br>
      <table border='1'>
        <tr><td>{{ t11 }}</td><td>{{ t12 }}</td><td>{{ t13 }}</td></tr>
        <tr><td>{{ t21 }}</td><td>{{ t22 }}</td><td>{{ t23 }}</td></tr>
        <tr><td>{{ t31 }}</td><td>{{ t32 }}</td><td>{{ t33 }}</td></tr>

      </table>
   <button v-if='t11==="X" || t11==="O"' disabled  >{{ turn }}</button>
   <button  v-else v-on:click='t11 =turn,msg+=1'>{{ turn }}</button>
   <button v-if='t12==="X" || t12==="O"' disabled  >{{ turn }}</button>
   <button  v-else v-on:click='t12 =turn,msg+=1'>{{ turn }}</button>
   <button v-if='t13==="X" || t13==="O"' disabled  >{{ turn }}</button>
   <button  v-else v-on:click='t13 =turn,msg+=1'>{{ turn }}</button>
<br>
<button v-if='t21==="X" || t21==="O"' disabled  >{{ turn }}</button>
<button  v-else v-on:click='t21 =turn,msg+=1'>{{ turn }}</button>
<button v-if='t22==="X" || t22==="O"' disabled  >{{ turn }}</button>
<button  v-else v-on:click='t22 =turn,msg+=1'>{{ turn }}</button>
<button v-if='t23==="X" || t23==="O"' disabled  >{{ turn }}</button>
<button  v-else v-on:click='t23 =turn,msg+=1'>{{ turn }}</button>
<br>
<button v-if='t31==="X" || t31==="O"' disabled  >{{ turn }}</button>
<button  v-else v-on:click='t31 =turn,msg+=1'>{{ turn }}</button>
<button v-if='t32==="X" || t32==="O"' disabled  >{{ turn }}</button>
<button  v-else v-on:click='t32 =turn,msg+=1'>{{ turn }}</button>
<button v-if='t33==="X" || t33==="O"' disabled  >{{ turn }}</button>
<button  v-else v-on:click='t33 =turn,msg+=1'>{{ turn }}</button>
<br>
<button v-on:click='msg = 0,t11="",t12="",t13="",t21="",t22="",t23="",t31="",t32="",t33=""'>Reset</button>
<br>
    </div></center>
  </section>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      turn: 'X',
      // if(msg%2==0){'X'}
      // else{'O'}
      msg: 0
    }
  },
  components: {
  }
}
</script>

<style>
.program{
  margin-top: 20px;
}
button {
  margin-top: 10px;
  width: 60px;
  height: 40px;

}
td{
    margin-top: 10px;
    width: 60px;
    height: 40px;
}
</style>
