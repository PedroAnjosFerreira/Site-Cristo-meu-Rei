<script>
  import answers from "./stores";

  let id = "Fé";
  let min = 0;
  let max = 10;
  let step = 1;
  let val = 5;

  export let cont;

  let resposta;
  let respostaa;
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
    nextDisabled = true;
  }
  function get_answers() {
    cont += 1;

    $answers = [...$answers, resposta, val];
  }
</script>

<div class="w-full max-w-xl">
  <h1 class="font-bold text-5xl text-center text-emerald-600 drop-shadow-sm">
    Seja um Cristão melhor
  </h1>
  <div class="bg-white p-12 rounded-lg shadow-lg w-full mt-8">
    <h1 class="text-2xl font-bold">Você crê em Deus?</h1>
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
          class="block mt-4 border bg-green-400/75 cursor-pointer border-gray-300 rounded-lg py-2 px-6 text-lg"
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
          >Não</label
        >
      {:else}
        <label
          for="não"
          class="block mt-4 bg-red-500/75 cursor-pointer border border-gray-300 rounded-lg py-2 px-6 text-lg"
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
      {#if yes_selected == true}
        <h1 class="text-2xl font-bold mt-4">
          De 0 a 10, qual nota você daria à sua Fé
        </h1>
        <div class=" mt-2">
          <input
            class="accent-emerald-600 w-full"
            type="range"
            {id}
            {min}
            {max}
            {step}
            name={id}
            bind:value={val}
          />
          <div class="text-lg font-semibold flex justify-between">
            <span class="text-neutral-400">0</span>
            <span class="text-emerald-700">{val}</span>
            <span class="text-neutral-400">10</span>
          </div>
        </div>
      {:else if resposta == "Não"}
        <iframe
          class="mt-5 aspect-video rounded-lg"
          width="100%"
          src="https://www.youtube.com/embed/PAPhq0Q6NsQ"
          title="Acredite no seu Salvador"
          frameborder="0"
          autoplay={true}
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        />
      {/if}
    </form>
    <button
      disabled={nextDisabled}
      id="botão"
      class="disabled:opacity-30 bg-white hover:bg-gray-100 text-gray-800 font-semibold py-2 px-4 border border-gray-400 rounded mt-5 shadow"
      on:click={get_answers}>Próxima</button
    >
  </div>
</div>
