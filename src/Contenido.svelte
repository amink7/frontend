<script>
  import { Route }  from "svelte-routing";
  import Inicio     from "./Inicio.svelte";
  import Armas  from "./Armas.svelte";
  import Soldados   from "./Soldados.svelte";
</script>

<style>
  main {
    padding: 20px;
    padding-top: 50px;
  }
</style>

<main id="contenido">
  <Route path="/" component={Inicio} />
  <Route path="/armas" component={Armas} />
  <Route path="/soldados" component={Soldados} />
</main>
