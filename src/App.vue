<template>
  <div id="app">
    <div class="bg-black text-white w-full p-4 h-32 mb-2">
      <Header :titulo="titulo" :entrega="entrega" />
    </div>
    <Tabla :tabla="tree.tabla" />
    <Tabla :tabla="one.tabla" />
    <Tabla :tabla="two.tabla" />
  </div>
</template>

<script>
import Tabla from './components/MyTabla.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Tabla,
    Header
  },
  data() {
        return {
            titulo: 'Name : Angel Nicolas Jimenez',
            entrega: 'Esta es la Tercera entrega - Componentes con VueJs CLI',
            one: {
                tabla: {
                    title: 'Tabla de datos con Componentes - Hamburguesas',
                    headtable: ['Index', 'Imagen', 'Descripcion', 'Precio'],
                    productos: 
                    [
                        {
                            url: '../src/assets/image/hamburguesa.jpg',
                            descripcion: 'Hamburguesa simple',
                            precio: 100
                        },
                        {
                            url: '../src/assets/image/hamburguesa.jpg',
                            descripcion: 'Hamburguesa doble',
                            precio: 200
                        },
                        {
                            url: '../src/assets/image/hamburguesa.jpg',
                            descripcion: 'Hamburguesa triple',
                            precio: 300
                        }
                    ],
                    fondo: 'bg-yellow-300'
                }
            },
            two: {
                tabla: {
                    title: 'Tabla de datos con Componentes - Autos',
                    headtable: ['Index', 'Imagen', 'Descripcion', 'Precio'],
                    productos: [
                        {
                            url: '../src/assets/image/audi.jpg',
                            descripcion: 'Audi A4',
                            precio: 58000
                        },
                        {
                            url: '../src/assets/image/audi.jpg',
                            descripcion: 'Audi A5',
                            precio: 68000
                        },
                        {
                            url: '../src/assets/image/audi.jpg',
                            descripcion: 'Audi A5',
                            precio: 78000
                        }
                    ],
                    fondo: 'bg-orange-300'
                }
            },
            tree: {
                tabla: {
                    title: 'Tabla de datos con Componentes - Usuarios',
                    headtable: ['Index', 'Nombre', 'Apellido', 'Edad'],
                    usuarios: [
                        {
                            nombre: 'Felipe',
                            apellido: 'Jimenez',
                            edad: 58
                        },
                        {
                            nombre: 'Andres',
                            apellido: 'Ramirez',
                            edad: 35
                        },
                        {
                            nombre: 'Juan',
                            apellido: 'Rodriguez',
                            edad: 17
                        }
                    ],
                    fondo: 'bg-lime-300'
                }
            }
        }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
