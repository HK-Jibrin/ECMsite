<template>
  <div>
      <ul class="list-group">
  <li class="list-group-item"> {{ category.name }}</li>
</ul>
   </div> 
</template>
<script>
export default {
   props: ['category'],
}
</script>

<style>
.list-group{
    width: 50%;
    height: 50px;
   
}
</style>