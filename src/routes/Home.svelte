<script>
  import answers from "../lib/stores";

  import Question1 from "../lib/Question_1.svelte";
  import Question2 from "../lib/Question_2.svelte";
  import Question3 from "../lib/Question_3.svelte";
  import Question4 from "../lib/Question_4.svelte";

  let contador = 1;
</script>

<main>
  <div class="antialiased text-gray-700 bg-gray-100">
    <div class="flex w-full h-screen justify-center items-center">
      {#if contador == 1}
        <Question1 bind:cont={contador} />
      {:else if contador == 2}
        <Question3 bind:cont={contador} />
      {:else if contador == 3}
        <Question2 bind:cont={contador} />
      {:else if contador == 4}
        <Question4 bind:cont={contador} />
      {/if}
    </div>
    <span
      >Esta página, e qualquer produto que se associe à mesma não tem qualquer
      relação com qualquer figura pública, que possa ter aparecida associada à
      página</span
    >
  </div>
</main>
