<script>
  import { onMount, getContext } from "svelte";
  import { jsonData }            from "./store.js";

  import Buscar                  from "./Buscar.svelte";
  import Arma                from "./Arma.svelte";
  import Boton                   from "./Boton.svelte";

  const URL = getContext("URL");

  let busqueda = "";
  let arma = {};

  onMount(async () => {
    const response = await fetch(URL.armas);
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

<h1>ARMAS</h1>
<Buscar bind:busqueda />

<div class="container">
  <Arma bind:arma>
    <div style="text-align: right">
      <Boton documento={arma} tipo="insertar" coleccion="armas" />
    </div>
  </Arma>
</div>

<div class="container">
  {#each datos as arma}
    <Arma {arma}>
      <div style="text-align: right">
        <Boton documento={arma} tipo="modificar" coleccion="armas" />
        <Boton documento={arma} tipo="eliminar"  coleccion="armas" />
      </div>
    </Arma>
  {/each}
</div>
