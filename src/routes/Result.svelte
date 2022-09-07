<script>
  import answers from "../lib/stores";
  import Course from "../lib/Course.svelte";

  var fe = $answers[1];
  var tempo = $answers[2];
  var filhos = $answers[4] === "Sim";
  var pregar = $answers[5] === "Sim";
</script>

<div class="bg-gray-50 p-6 mx-auto max-w-5xl">
  <h1 class="font-bold text-5xl mb-3 animate-pulse">
    Melhores opções para você
  </h1>
  <h2 class="text-xl mb-6 text-gray-600">
    Esta é uma seleção dos melhores cursos do mercado que satisfazem suas
    vontades
  </h2>

  <div class="flex flex-col space-y-4">
    <Course
      title="Destravando seu conhecimento bíblico + Biblia todo dia"
      description="Para você que tem dificuldade de entender o texto biblico e de arranjar tempo e disposição para dedicar à palavra do senhor"
      productUrl="https://go.hotmart.com/F74381876P?ap=b43a"
      imageUrl="https://static-media.hotmart.com/YfUxVuy95C2n9yIeHzWPK84MHaU=/filters:background_color(white)/hotmart/product_pictures/0b728954-a26c-48ef-a95c-cd4dba562eb8/LogoDSEB.png"
      price={300}
    />
    {#if filhos}
      <Course
        title="Escolinha Bíblica Infantil"
        description="Para você que quer ensinar a palavra de Deus para seus filhos da melhor forma possível"
        productUrl="https://go.hotmart.com/U74544698Q"
        imageUrl="https://static-media.hotmart.com/KsY_HO4wFPwiqC3GbMRxTKjTGK8=/filters:background_color(white)/hotmart/product_pictures/421ead8d-6c1d-433b-a6bd-cc1adacc5bb4/ESCOLINHABBLICAVOLUME25.png"
        price={10}
      />
    {/if}
    {#if pregar}
      <Course
        title="Curso Pregador Vocacionado + Curso IBGA"
        description="Para você que tem interesse em se aprofundar mais na palavra espalhar a graça do senhor da melhor maneira possível"
        productUrl="https://go.hotmart.com/A74544707S"
        imageUrl="https://static-media.hotmart.com/P0PZEVAntcXPVH6KFwnXmt9SLiE=/filters:background_color(white)/hotmart/product_pictures/3921d141-9101-49c7-b150-6f3118b4bb21/65decomisso4.png"
        price={113}
      />
    {/if}
  </div>
</div>
