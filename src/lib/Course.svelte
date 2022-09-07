<script>
  export let title;
  export let description;
  export let productUrl;
  export let imageUrl;
  export let price;

  const intlNumberFormat = Intl.NumberFormat("pt-BR", {
    style: "currency",
    currency: "BRL",
  });

  $: formattedPrice = intlNumberFormat.format(price);
</script>

<a target="_blank" href={productUrl} class="hover:opacity-80">
  <div
    class="flex flex-col md:flex-row border border-neutral-200 bg-white rounded-md shadow-sm overflow-hidden"
  >
    <img class="w-full md:w-64 h-64 object-cover" src={imageUrl} alt={title} />
    <div class="flex flex-col justify-between p-4">
      <div>
        <h1 class="font-bold text-2xl">{title}</h1>
        <p class="text-neutral-500 mt-2">{description}</p>
      </div>
      <span class="font-extrabold text-2xl mt-4">{formattedPrice}</span>
    </div>
  </div>
</a>
