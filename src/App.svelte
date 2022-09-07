<script>
  import Router from "svelte-spa-router";

  import Home from "./routes/Home.svelte";
  import Result from "./routes/Result.svelte";

  const routes = {
    "/": Home,
    "/result": Result,
  };
</script>

<Router {routes} />
