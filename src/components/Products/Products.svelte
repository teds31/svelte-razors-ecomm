<script>
  //   import { onMount, onDestroy } from "svelte";
  import Product from "./Product.svelte";
  import products from "../../stores/defaultProducts";
  export let title = "";
  let localProducts = $products;

  //   onMount(() => {
  //     unsubscribe = products.subscribe((value) => {
  //       localProducts = value;
  //     });
  //   });
  //   onDestroy(() => {
  //     unsubscribe();
  //   });
</script>

<section class="section">
  <h2 class="section-title">{title}</h2>
  <div class="products-center">
    {#each $products as product (product.id)}
      <Product {product} />
    {/each}
  </div>
</section>

<style>
  img {
    height: auto;
    width: 25%;
  }
</style>
