<template>
  <div class="home">
  <Header/>
  <div class="container">
  <div class="row">
    <div class="col-md-4" with= 50s%><category v-for="cat in categories" :key="cat.id" :category="cat"/></div>
    <div class="col-md-8"><Carousel/></div>
  </div>
    </div>  
  <div class="items">
    <Product v-for="item in products" :key="item.id" :products="item" />
  </div> 
   <Footer/>
  </div>
</template>
<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Category from '@/components/Category.vue'
import Product from '@/components/Product.vue'
import Carousel from '../components/Carousel.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
   Header,
   Category,
   Product,
   Carousel,
   Footer

  },
  data(){
      return{

        categories: [
          {
            id : 1,
        name: 'G-wagon',
        
          
        },
        {
            id : 2,
        name: "Made in Nigeria Cars  ",
        
        },
        {
            id : 3,
        name: 'Sports Cars made in Nigeria',
        
          
        },
    {
            id : 4,
        name: 'Power Bike',
        
          
        },
        {
            id : 5,
        name: "SUV",
        
           },
            {
            id : 6,
        name: "Range Rover",
            }
        ],

    products: [
        {
        id: 1,
        imageLink: require("../assets/Gwogon.jpg") ,
        name: 'G-wagon',
        price: '200 million'
        },
         {
         id: 2,
         imageLink: require("../assets/made1.jpg") ,
        name: 'Made in Nigeria',
        price: 800000
         },
        {
        id: 3,
        imageLink: require("../assets/made2.jpg") ,
        name: 'Sport car made in Nigeria',
        price: '3.6 million'
        },
        {
        id: 4,
        imageLink: require("../assets/Suv.jpg") ,
        name: 'SUV',
        price: '20 million'
        },
        {
        id: 6,
        imageLink: require("../assets/made4_640.jpg") ,
        name: 'Toyota Mirai',
        price: '120 million'
        },
        {
        id: 7,
        imageLink: require("../assets/range.jpg") ,
        name: 'Range Rover',
        price: '150 million'
        },
        {
        id: 8,
        imageLink: require("../assets/powerbike.jpg") ,
        name: 'Power Bike',
        price: '15 million'
        },
        {
        id: 9,
        imageLink: require("../assets/flying.jpg") ,
        name: 'Flying Spur',
        price: '350 million'  
        },
         {
        id: 10,
        imageLink: require("../assets/benz.jpg"),
        name: 'Mercedees benz c300',
        price: '75.7 million'
        },{
        id: 11,
        imageLink: require("../assets/suzukibrezza.jpg") ,
        name: 'Suzuki Brezza',
        price: '25.9 million'
        },
    ]

    }
  }

  }
</script>

<style>

.down{
  margin: 0px;
}
.bv-example-row{
 margin-top: 10px;
}
.items{
  display: inline;
}

</style>
