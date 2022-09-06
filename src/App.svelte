<script>
  import Router from "svelte-spa-router";
  import Home from "./routes/Home.svelte";
  import answers from "./lib/stores";

  import { wrap } from "svelte-spa-router/wrap";

  const routes = {
    "/": Home,
    "/Result/*": wrap({
      asyncComponent: () => import("./routes/Result.svelte"),
    }),
  };
</script>

<main>
  <Router {routes} />
</main>
