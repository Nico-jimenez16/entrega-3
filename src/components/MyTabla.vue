<template>
    <div>
        <div class="mb-8">
            <h1 class="flex w-full justify-center items-center text-3xl p-4">{{ tabla.title }}</h1>
            <div>
                <table class="w-full table-auto text-xl">
                    <thead class="h-full bg-black text-white p-8">
                        <tr>
                            <th v-for="(head, i) of tabla.headtable" :key="i" scope="col">{{head}}</th>
                        </tr>
                    </thead>

                    <!-- Tabla de Productos -->

                    <tbody class="flex-inline text-2xl" :class="[tabla.fondo]">
                        <tr v-for="(producto, index) of tabla.productos" :key="index">
                            <td>{{index + 1}}</td>
                            <td><img class="w-1/2 m-auto" :src="getimage(producto)"></td>
                            <td>{{producto.descripcion}}</td>
                            <td>$ {{producto.precio}}</td>
                        </tr>

                    <!-- Tabla de Usuarios -->

                        <tr v-for="(usuario, index) of tabla.usuarios" :key="index">
                            <td>{{index + 1}}</td>
                            <td>{{usuario.nombre}}</td>
                            <td>{{usuario.apellido}}</td>
                            <td>{{usuario.edad}}</td>
                        </tr>
                    </tbody>
                </table>
            </div>   
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyTabla',
    props: {
        tabla:{
            type: Object,
            required: true
        }
    },
    methods: {
      getimage(p){
          return require(`@/assets/image/${p.url}`)
      }
    }
}
</script>

<style scoped>
tr{
    display: flex;
    height: 100%;
}

th, td{
    border: 1px solid;
    width: 100%;
    padding: 10px;
}
td {
    text-align: center;
}
</style>