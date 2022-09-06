<script>
  import answers from "./stores";

  export let cont;

  let resposta;
  let yes_selected = false;
  let no_selected = false;
  let nextDisabled = true;

  function yes_button_selected() {
    resposta = "Sim";
    yes_selected = true;
    no_selected = false;
    nextDisabled = false;
  }
  function no_button_selected() {
    resposta = "Não";
    no_selected = true;
    yes_selected = false;
    nextDisabled = false;
  }
  function get_answers() {
    cont += 1;

    $answers = [...$answers, resposta];
  }
</script>

<div class="w-full max-w-xl">
  <h1 class="font-bold text-5xl text-center text-indigo-700">
    Seja um Cristão melhor
  </h1>
  <div class="bg-white p-12 rounded-lg shadow-lg w-full mt-8">
    <h1 class="text-2xl font-bold">
      Na sua opinião, você dedica tempo suficiente para Deus?
    </h1>
    <form>
      {#if yes_selected == false}
        <label
          for="sim"
          class="block mt-4 border border-gray-300 rounded-lg py-2 px-6 text-lg "
          >Sim</label
        >
      {:else}
        <label
          for="sim"
          class="block mt-4 border bg-green-400/75 border-gray-300 rounded-lg py-2 px-6 text-lg"
          >Sim</label
        >
      {/if}
      <input
        on:click={yes_button_selected}
        type="radio"
        name="escolha"
        id="sim"
        class="hidden"
      />
      {#if no_selected == false}
        <label
          for="não"
          class="block mt-4 border border-gray-300 rounded-lg py-2 px-6 text-lg"
          >não</label
        >
      {:else}
        <label
          for="não"
          class="block mt-4 bg-red-500/75 border border-gray-300 rounded-lg py-2 px-6 text-lg"
          >Não</label
        >
      {/if}
      <input
        on:click={no_button_selected}
        type="radio"
        name="escolha"
        id="não"
        class="hidden"
      />
    </form>
    <button
      disabled={nextDisabled}
      class="disabled:opacity-30 bg-white hover:bg-gray-100 mt-5 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow"
      on:click={get_answers}>Próxima</button
    >
  </div>
</div>
