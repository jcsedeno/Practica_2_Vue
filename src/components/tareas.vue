<template>
    <div id="tablaTareas">
        <table class="warning">
            <thead>
                <tr>
                    <th>nombre</th>
                    <th>tiempo</th>
                    <th>colaborador</th>
                </tr>
            </thead>
            <tbody>
               <tr v-for="tarea in tareas" :key='tarea.id'>
                   <td>{{tarea.nombre}} </td>
                   <td>{{tarea.tiempo}} </td>
                   <td>{{tarea.colaborador}} </td>


               </tr>
                           </tbody>
        </table>

    </div>
</template>

<script>
export default {
    name: "#tablaTareas",
    props: ['tareas']
}
</script>

<style scoped>
    tbody{
        background-color: aliceblue;
        
    }
</style>