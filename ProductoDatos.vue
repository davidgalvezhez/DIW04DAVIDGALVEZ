<template>
  <section id="producto-datos">
      <h1>ZAPATILLAS FÚTBOL SALA - TRUENO</h1>
      <h2>25,99€</h2>
      <div class="wrapper">
          <button class="btn" @click="cambiarContador('-1')" type="button" name="button">-</button>
          <input class="cantidad" type="text" name="name" :value="contador">
          <button class="btn" @click="cambiarContador('1')" type="button" name="button">+</button>
      </div>
      <br>
      <button class="boton"><span class="material-icons"></span> AÑADIR AL CARRITO</button>
  </section>
</template>

<script>
export default {
  Name: 'ProductoDatos',
    data () {
        return {
            contador: 1
        }
    },
    methods: {
        cambiarContador(num) {
            this.contador += +num;
            if (!isNaN(this.contador) && (this.contador < 0)) {
              this.contador = 0
            }
        }
    }
}
</script>

<style scoped>
section#producto-datos {
  flex: 1 1 18rem;
}
h1 {
  font-size: arial;
}
h2 {
  font-size: arial;
  color: black;
}
span.iva {
  font-size:1rem;
  font-weight: normal;
  color: #282828
}
.wrapper {
  height: 2rem;
  display: flex;
}
.cantidad {
  border: none;
  text-align: center;
  width: 2rem;
  font-size: 1.2rem;
  border: 1px solid #000000;
}
.btn {
  border: 1px solid #a39797;
  width: 1.8rem;
}
button:focus, input:focus {
  outline: 0;
 
}
.boton {
  background-color: black;
  color: #ffffff;
}
</style>