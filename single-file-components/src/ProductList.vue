<template>
	<div class="product-list">
    <h2>{{title}}</h2>
    <ul>
      <product-list-item v-for="(product, i) in products" @remove="remove(i)" :product="product">
      </product-list-item>
    </ul>
  </div>
</template>

<script>
	import ProductListItem from './ProductListItem.vue';

	export default {
		name: "product-list",
		props: ['products', 'title'],
        methods: {
            remove: function(i) {
              this.products.splice(i, 1);
            }
        } 
	};

</script>

<style scoped>
  h2 {
    margin-bottom: 40px;
  }

  ul {
    list-style-type: none;
  }
</style> 