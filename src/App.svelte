<script>
  import { setContext } from "svelte";
  import { Router }     from "svelte-routing";
  import Nav            from "./Nav.svelte";
  import Contenido      from "./Contenido.svelte";
  
  const URL = {
    articulos :  "https://backendpwa-production-c373.up.railway.app/api/articulos/",
    clientes :   "https://backendpwa-production-c373.up.railway.app/api/clientes/"
  };

  setContext("URL", URL);
</script>

<Router>
  <Nav />
  <Contenido />
</Router>



<style>
  @import url("https://fonts.googleapis.com/css?family=Arial");

  :global(body) {
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    font-family: "Arial";
    font-display: swap;     /* Para mejorar rendimiento en carga inicial */
  }

  :global(*) {
    margin: 0;
    padding: 0;
  }

  :global(a:hover) {
    text-decoration: none;
    cursor: pointer;
  }

  :global(div#OK, div#KO) {
    display: none;
    position: fixed;
    top: 60px;
    right: 0px;
    font-size: 60px;
    background-color: transparent;
  }
</style>
