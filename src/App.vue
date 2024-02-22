<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: '+',
      resultado: 0
    }
  },
  methods: {
    calcular() {
      switch (this.operacao) {
        case '+':
          this.resultado = parseInt(this.numero1) + parseInt(this.numero2);
          break;
        case '-':
          this.resultado = parseInt(this.numero1) - parseInt(this.numero2);
          break;
        case '*':
          this.resultado = parseInt(this.numero1) * parseInt(this.numero2);
          break;
        case '/':
          this.resultado = parseInt(this.numero1) / parseInt(this.numero2);
          break;
      }
    }
  }
}
</script>

<template>
  
    
  <div id="app">
    <h2>Calculadora Aritmetrica Basica</h2>
  <div class="cal">
    <input type="number" v-model.number="numero1" @input="calcular">
    <input type="number" v-model.number="numero2" @input="calcular">
    <select v-model="operacao" @change="calcular">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
    </select>
  </div>
    <p>Resultado: {{ resultado }}</p>
  </div>

</template>

<style scoped>

#app{
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 8%;
  background-color: rgb(235, 232, 227);
  border-radius: 7px;
  height: 60vh;
  
}

.cal{
  display: flex;
}

h2{
  margin-bottom: 4%;
}

p{
  font-size: 25px;
  color: green;
}

input{
  font-size: 25px;
  padding-left: 2%;
  margin-right: 1%;
  border: none;
  border-radius: 5px;
  background-color: orange;
  font-weight: bold;
}

select{
  font-size: 25px;
  border: none;
  border-radius: 5px;
  background-color: blue;
  color: #fff;
}

</style>
