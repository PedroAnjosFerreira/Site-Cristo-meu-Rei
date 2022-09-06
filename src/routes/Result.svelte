<script>
  import answers from "../lib/stores";

  var _answers = $answers;
  var fe = _answers[1];
  var tempo = _answers[2];
  var filhos = _answers[4];
  var pregar = _answers[5];
</script>

<main>
  <div class="antialiased text-gray-700 bg-gray-100">
    <h1 class="font-bold text-5xl text-center text-emerald-600 ">
      Melhores opções para você
    </h1>

    <div class="w-full h-screen justify-center items-center">
      <div
        on:click={() => (window.location.href = "")}
        class="md:flex lg:flex w-5/6 bg-white p-1 ml-10 mr-10 rounded-lg shadow-lg mt-8"
      >
        <img
          class="sm:w-full md:w-1/4 lg:w-1/4"
          src="https://static-media.hotmart.com/YfUxVuy95C2n9yIeHzWPK84MHaU=/filters:background_color(white)/hotmart/product_pictures/0b728954-a26c-48ef-a95c-cd4dba562eb8/LogoDSEB.png"
          alt="Destravando conhecimento biblico biblia"
        />
        <div class="flex flex-col justify-between p-4">
          <div>
            <h1 class="font-bold text-2xl">
              Destravando seu conhecimento bíblico + Biblia todo dia
            </h1>
            <p class="font-thin text-neutral-500 mt-2">
              Para você que tem dificuldade de entender o texto biblico e de
              arranjar tempo e disposição para dedicar à palavra do senhor
            </p>
          </div>
          <button
            class="bg-transparent hidden md:block hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
            ><a href="https://go.hotmart.com/F74381876P?ap=b43a">Comprar</a
            ></button
          >
          <span class="text-center font-extrabold text-2xl">300,09 R$</span>
        </div>
      </div>
      {#if filhos == "Sim"}
        <div
          class="md:flex lg:flex w-5/6 bg-white p-1 ml-10 mr-10 rounded-lg shadow-lg mt-8"
        >
          <img
            class="sm:w-full md:w-1/4 lg:w-1/4"
            src="https://static-media.hotmart.com/KsY_HO4wFPwiqC3GbMRxTKjTGK8=/filters:background_color(white)/hotmart/product_pictures/421ead8d-6c1d-433b-a6bd-cc1adacc5bb4/ESCOLINHABBLICAVOLUME25.png"
            alt="Destravando conhecimento biblico biblia"
          />
          <div class="flex flex-col justify-between p-4">
            <div>
              <h1 class="font-bold text-2xl">Escolinha Bíblica Infantil</h1>
              <p class="font-thin text-neutral-500 mt-2">
                Para você que quer ensinar a palavra de Deus para seus filhos da
                melhor forma possível
              </p>
            </div>
            <button
              class=" bg-transparent hidden md:block hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
              ><a href="https://go.hotmart.com/U74544698Q">Ver mais</a></button
            >
            <span class="font-extrabold text-center block text-2xl">10 R$</span>
          </div>
        </div>
      {/if}
      {#if pregar == "Sim"}
        <div
          class="md:flex lg:flex w-5/6 bg-white p-1 ml-10 mr-10 rounded-lg shadow-lg mt-8"
        >
          <img
            class="sm:w-full md:w-1/4 lg:w-1/4"
            src="https://static-media.hotmart.com/P0PZEVAntcXPVH6KFwnXmt9SLiE=/filters:background_color(white)/hotmart/product_pictures/3921d141-9101-49c7-b150-6f3118b4bb21/65decomisso4.png"
            alt="Destravando conhecimento biblico biblia"
          />
          <div class="flex flex-col justify-between p-4">
            <div>
              <h1 class="font-bold text-2xl">
                Curso Pregador Vocacionado + Curso IBGA
              </h1>
              <p class="font-thin text-neutral-500 mt-2">
                Para você que tem interesse em se aprofundar mais na palavra e
                espalhar a graça do senhor da melhor maneira possível
              </p>
            </div>
            <button
              class="bg-transparent hidden md:block hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded"
              ><a href="https://go.hotmart.com/A74544707S">Ver mais</a></button
            >
            <span class="text-center font-bold text-2xl">113,10 R$</span>
          </div>
        </div>
      {/if}
    </div>
  </div>
</main>
