<script>
  import { onMount, getContext } from "svelte";
  import { jsonData }            from "./store.js";

  import Buscar                  from "./Buscar.svelte";
  import Soldado                 from "./Soldado.svelte";
  import Boton                   from "./Boton.svelte";

  const URL = getContext("URL");

  let busqueda = "";
  let soldado = {};

  onMount(async () => {
    const response = await fetch(URL.soldados);
    const data = await response.json();
    $jsonData = data;
  });

  $: regex = new RegExp(busqueda, "i");
  $: datos = busqueda 
    ? $jsonData.filter(item => regex.test(item.nombre))
    : $jsonData;

</script>

<style>
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: left;
    flex-wrap: wrap;
  }
</style>

<h1>SOLDADOS</h1>
<Buscar bind:busqueda />

<div class="container">
  <Soldado bind:soldado>
    <div style="text-align: right">
      <Boton documento={soldado} tipo="insertar" coleccion="soldados" />
    </div>
  </Soldado>
</div>

<div class="container">
  {#each datos as soldado}
    <Soldado {soldado}>
      <div style="text-align: right">
        <Boton documento={soldado} tipo="modificar" coleccion="soldados" />
        <Boton documento={soldado} tipo="eliminar" coleccion="soldados" />
      </div>
    </Soldado>
  {/each}
</div>