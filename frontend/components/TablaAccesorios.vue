<template>
  <div>
   <v-data-table
        v-bind:headers="headers"
        :items="items"
        hide-actions
        class="elevation-1"
    >
      <template slot="items" scope="props">
        <td style="font-weight: bold;">{{ props.item.name }}</td>
        <td class=""><v-radio label="" v-model="props.item.modelo" value="SI"></v-radio></td>
        <td class=""><v-radio label="" v-model="props.item.modelo" value="NO"></v-radio></td>
      </template>
   </v-data-table>
   
   
  </div>
</template>

<script>
  export default {
    data () {
      return {
        headers: [
          {
            text: 'ACCESORIOS',
            align: 'left',
            sortable: false,
            value: 'name'
          },
          { text: 'SI',align:"left",sortable:false },
          { text: 'NO',align:"left",sortable:false},
        ],
        items: [
          {
            name: 'HERRAMIENTAS', 
            modelo: "SI",
          },
          {
            name: 'ESPEJOS',
            modelo: "SI",
          },
          {
            name: 'LLAVES',
            modelo: "SI",
          },
          {
            name: 'TAPAS LATERALES',
            modelo: "SI",
          },
          {
            name: 'COCAS',
            modelo: "SI",
          },
          {
            name: 'TAPA GASOLINA Y/O ACEITE',
            modelo: "SI",
          },
          {
            name: 'GUARDACADENA',
            modelo: "SI",
          },
        ]
      }
    }
  }
</script>