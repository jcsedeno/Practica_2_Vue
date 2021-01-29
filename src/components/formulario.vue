<template>
  <div id="formularioTareas">
    <form @submit.prevent="enviarFormulario">
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <div class="form-group">
              <label for="">nombre</label>
              <input class="form-control" type="text" v-model="tarea.nombre" />
              
            </div>
          </div>
          <div class="col-md-4">
            <div class="form-group">
              <label for="">tiempo</label>
              <input class="form-control" type="text" v-model="tarea.tiempo" />

            </div>
          </div>
          <div class="col-md-4">
            <div class="form-group">
              <label for="">colaborador</label>
              <input class="form-control" type="text" v-model="tarea.colaborador" />

              <input type="button" value="boton">
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
    export default{
        name: '#formularioTareas',
    data(){
      return{
        tarea:{
          nombre:'',
          tiempo:'',
          colaborador:''
        }
      }

    },

    method: {
      enviarFormulario(){
        this.$emit(' agregarTarea', this.tarea),
        console.log('enviado')
      }
    }

    }
    </script>

