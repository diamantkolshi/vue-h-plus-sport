<template>
	<li>
     <img :src="product.image">
    <p><strong>{{product.name}}</strong></p>
    <p>description of {{product.name}} </p>
    <a @click="requestRemoval">Hide this item</a>
  </li>
</template>

<script type="text/javascript">
 export default {
 	name: 'product-list-item',
 	props: ['product'],
    methods: { 
      requestRemoval: function() {
        this.$emit('remove')
      }
    }
 };
</script>

<style scoped>
    img {
        float: left;
        width: 300px;
    }
    li {
        margin-bottom: 40px;
        clear: both;
    }

</style>       