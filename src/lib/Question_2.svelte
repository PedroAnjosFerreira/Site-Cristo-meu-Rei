<script>
  import answers from "./stores";

  export let cont;

  let resposta;
  let respostaa;
  let yes_selected = false;
  let no_selected = false;
  let yes_selected2 = false;
  let no_selected2 = false;
  let nextDisabled = true;

  function yes_button_selected() {
    resposta = "Sim";
    yes_selected = true;
    no_selected = false;
  }
  function no_button_selected() {
    resposta = "Não";
    no_selected = true;
    yes_selected = false;
    nextDisabled = false;
  }
  function yes_button_selected2() {
    respostaa = "Sim";
    yes_selected2 = true;
    no_selected2 = false;
    nextDisabled = false;
  }
  function no_button_selected2() {
    respostaa = "Não";
    no_selected2 = true;
    yes_selected2 = false;
    nextDisabled = false;
  }

  function get_answers() {
    cont += 1;

    $answers = [...$answers, resposta, respostaa];
  }
</script>

<div class="w-full max-w-xl">
  <h1 class="font-bold text-5xl text-center text-indigo-700">
    Seja um Cristão melhor
  </h1>
  <div class="bg-white p-12 rounded-lg shadow-lg w-full mt-8">
    <h1 class="text-2xl font-bold">Você tem filhos pequenos?</h1>
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
          >não</label
        >
      {/if}
      <input
        on:click={no_button_selected}
        type="radio"
        name="escolha"
        id="não"
        class="hidden"
      />
      {#if yes_selected == true}
        <h1 class="text-1xl font-bold pt-3">
          Gostaria de aprender a melhor maneira de ensinar a palavra para os
          seus filhos?
        </h1>
        {#if yes_selected2 == false}
          <label
            for="sim2"
            class="block mt-4 border border-gray-300 rounded-lg py-2 px-6 text-lg "
            >Sim</label
          >
        {:else}
          <label
            for="sim2"
            class="block mt-4 border bg-green-400/75 border-gray-300 rounded-lg py-2 px-6 text-lg"
            >Sim</label
          >
        {/if}
        <input
          on:click={yes_button_selected2}
          type="radio"
          name="escolha2"
          id="sim2"
          class="hidden"
        />
        {#if no_selected2 == false}
          <label
            for="não2"
            class="block mt-4 border border-gray-300 rounded-lg py-2 px-6 text-lg"
            >Não</label
          >
        {:else}
          <label
            for="não2"
            class="block mt-4 bg-red-500/75 border border-gray-300 rounded-lg py-2 px-6 text-lg"
            >não</label
          >
        {/if}
        <input
          on:click={no_button_selected2}
          type="radio"
          name="escolha2"
          id="não2"
          class="hidden"
        />
      {/if}
    </form>
    <button
      disabled={nextDisabled}
      class="disabled:opacity-30 bg-white hover:bg-gray-100 mt-5 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded shadow"
      on:click={get_answers}>Próxima</button
    >
  </div>
</div>
