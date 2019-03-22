<template>
  <div>
    <h1>HOLA {{msg}}</h1>
    <input type="text" v-model="msg">
    <button @click="guardar">Guardar</button>
    <table>
      <tr>
        <th>nombre</th>
      </tr>
      <tr v-for="(item, index) in municipio" :key="index">
          <td>
              {{item}}
          </td>
      </tr>
    </table>
  </div>
</template>
<script>
export default {
  data() {
    return {
      msg: "Yolanda Obando",
      municipio: ["mocoa", "villagarzon", "caicedo"]
    };
  },
  methods:{
      guardar(){
         // alert("guardando....#)

         this.municipio.push(this.msg)
         this.msg=''

      }
  }
};
</script>
