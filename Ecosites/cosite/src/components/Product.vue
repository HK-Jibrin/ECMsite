<template>
<div class="pro">
  <div class="product">
           <img :src="products.imageLink" height="150" width="250">
       <p>{{products.name}}  </p>
    <p> &#8358; {{products.price}} </p>
    <b-button class="btn btn-primary" @click="gotoProductDetails(products.id)"> Buy Now </b-button>  
   </div>
  </div>
</template>
<script>
export default {
 name: 'Product',
    props: ["products"],
    methods:{
        gotoProductDetails(productId) {
    this.$router.push({name:'products', params: {id:productId}})
    }
}
}
</script>

<style>
.product{
   padding: 0;
    margin: 0;
    margin-left: 10px;
    margin-bottom: 1px;
    border: 2px solid black;
    text-align: center;
    padding-top: 20px;
    background-color: whitesmoke;
    border-radius: 20px;
}
.pro{
   width: 300px; 
  margin-bottom: 10px;
  margin-right: 10px;
   display: inline-block;

}
</style>