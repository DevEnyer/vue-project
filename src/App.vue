<script setup>
  const titulo =  'Prueba de titulo 1' // Esto es solo una constante

  // Haciendo preba de una funcion sencilla 
  const buscarCosa = () =>{
    console.log('Estamos buscando la cosa');
  }
</script>

<template>
  <div class="flex items-center flex-col p-5">
    <h1 class="text-xl m-4">{{ titulo }}</h1> <!-- Aca llamamos a la constante del sector script -->
    <div class="flex items-center">
      <!--Esto es una input traido desde tailwind-->
      <input 
      type="text" 
      class="block min-w-0 grow py-1.5 pr-3 pl-1 text-base text-gray-900 placeholder:text-gray-400 focus:outline-none sm:text-sm/6" placeholder="Buscar...">
      <!-- Para colocar un evento Onclick solo hay que colocar @click -->
      <button @click = 'buscarCosa()' class="bg-blue-500 py-1.5 px-5" >Buscar</button> <!-- Aca se está haciendo uso de la función-->
    </div>
    <div class="m-6">
      <table class="table-fixed">
        <thead>
          <th>Foto</th>
          <th>Nombre</th>
          <th>Número</th>
          <th>Correo</th>
          <th>Acción</th>
        </thead>
        <tbody>
          <tr v-for="n in 20"> <!--Empezamos a usar las herramientas de Vue-->
            <td class="p-3 border-b-2">{{ n }}</td> <!--Se usa con el for-->
            <td class="p-3 border-b-2">Pepito</td>
            <td class="p-3 border-b-2">04123212121</td>
            <td class="p-3 border-b-2">correo@gmail.com</td>
            <td>
              <a href="#" class="py-2 px-4 bg-purple-900 rounded-full">Editar</a>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

</template>
