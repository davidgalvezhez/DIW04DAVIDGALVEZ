<template>
  <section id="producto-imagen">
      <div class="img-big"> 
          <img v-bind:src="fotos[0]" alt="Zapatillas Trueno Fútbol sala">
      </div>
        <div class="img-mini">
          <a @click="cambiarFoto(1)"><img  v-bind:src="fotos[1]" alt="Zapatillas Trueno Fútbol sala"></a>
          <a @click="cambiarFoto(2)"><img  v-bind:src="fotos[2]" alt="Zapatillas Trueno Fútbol sala"></a>
          <a @click="cambiarFoto(3)"><img  v-bind:src="fotos[3]" alt="Zapatillas Trueno Fútbol sala"></a>
          <a @click="cambiarFoto(4)"><img  v-bind:src="fotos[4]" alt="Zapatillas Trueno Fútbol sala"></a>
        </div>
      </section>    
</template>

<script>
export default {
    Name: 'ProductoImagen',
    data () {
        return {
            fotos: [
                require ('../assets/truenosala.jpg'),
                require ('../assets/truenosala.jpg'),
                require ('../assets/truenosala2.jpg'),
                require ('../assets/truenosala3.jpg'),
                require ('../assets/truenosala4.jpg')]
        }
    },
    methods: {
        cambiarFoto(id) {
            this.fotos[0] = this.fotos[id]
        }
    }
}
</script>

<style escoped>
#producto-imagen {
    border-radius: 25px;
    padding: 1rem;
    margin: 1rem;
    flex: 0 1 50%;
}
   

.img-mini {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    width: 750px;
    height: 100px;

    
}
.img-mini img {
    width: 100px;
    border:2px solid #837c7c;
}



</style>