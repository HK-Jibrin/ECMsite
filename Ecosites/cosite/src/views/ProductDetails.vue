
<template>
<div>
   <Header/>
   <div v-for = "product in products" :key="product.productId" >
     <div v-if="productId == product.productId">
       <div class="card flex-row flex-wrap">
        <div class="card-header border-0">
        <img :src="product.imageLink" height="400" alt="">
        <div id="small">
          <img :src="product.imageLink1" height="70"> &nbsp;
         <img :src="product.imageLink2" height="70"> &nbsp;
        <img :src="product.imageLink3" height="70">
        </div>
        </div>
        <div id="space" class="card-block px-2">
            <h4 class="card-title">{{product.name}}</h4>
            <label for="rating-1"><i class="fas fa-3x fa-star"></i></label>
            <label for="rating-2"><i class="fas fa-3x fa-star"></i></label>
            <label for="rating-3"><i class="fas fa-3x fa-star"></i></label>
            <label for="rating-4"><i class="fas fa-3x fa-star"></i></label>
            <h4>{{ product.price}}</h4>
           <a class="boo" text-variant="black">ADD TO CART <i class="fas fa-shopping-cart"></i></a>
        </div>
        <div class="w-100"></div>
        <div class="card-footer">
          <h1>Product Details</h1>
           <p class="card-text">{{product.Description}}</p>
        </div>
    </div>
     </div>
   </div>
   <Footer/>
  </div>
</template>
<script>
import Header from '../components/Header.vue'
import Footer from '../components/Footer'
 export default{
      props: ['proDetails'],
     
     components: {
         Header,
         Footer
      },

  data(){
   return{

    productId:this.$route.params.id,
     
   products: [
        {
        productId: 1,
        imageLink: require("../assets/Gwogon.jpg"),
        imageLink1: require("../assets/Gwogon.jpg"),
         imageLink2: require("../assets/Gwogon.jpg"),
          imageLink3: require("../assets/Gwogon.jpg"),
        name: 'G-wagon',
        Description: 'The new G-Class G 500 offers  fuel consumption around 12 liters per 100km.The interior is luxurious with all the modern twenty-first century appointments one could ask for, with long time insurance',
        price: '200 million'
        },
         {
         productId: 2,
         imageLink: require("../assets/made1.jpg"),
         imageLink1: require("../assets/made1.jpg"),
         imageLink2: require("../assets/made1.jpg"),
         imageLink3: require("../assets/made1.jpg"),
         Description: 'Seat Number – 5 to 7; Wheel Base – 3025; Engine Model – JM491Q – ME; Fuel – Gasoline; Max Power (km/rpm) – 76/4200 ῀ 4600; Max Torque (NU/rpm); Tank (70 liters) ',
        name: 'made in nigeria',
        price: '3.7 million.'
       
         },
        {
        productId: 3,
        imageLink: require("../assets/made2.jpg"),
        imageLink1: require("../assets/made2.jpg"),
        imageLink2: require("../assets/made2.jpg"),
        imageLink3: require("../assets/made2.jpg"),
         Description: 'This car it has air condition without comsuming fuel',
        name: 'Sport car made in Nigeria',
        price: '3.6 million'
        },
        {
        productId: 4,
        imageLink: require("../assets/Suv.jpg"),
        imageLink1: require("../assets/Suv.jpg"),
        imageLink2: require("../assets/Suv.jpg"),
        imageLink3: require("../assets/Suv.jpg"),
        Description: 'It has fuel economizer with speed limit of 7000k/h',
        name: 'SUV',
        price: '20 million'
        },
        {
        productId: 6,
        imageLink: require("../assets/made4_640.jpg"),
        imageLink1: require("../assets/made4_640.jpg"),
        imageLink2: require("../assets/made4_640.jpg"),
        imageLink3: require("../assets/made4_640.jpg"),
        Description: 'It has secondhand value even at old',
        name: 'Toyota Mirai',
        price: '120 million'
        },
        {
        productId: 7,
        imageLink: require("../assets/range.jpg"),
        imageLink1: require("../assets/range.jpg"),
        imageLink2: require("../assets/range.jpg"),
        imageLink3: require("../assets/range.jpg"),
        Description: 'with strong shock absorber and feel no pot holes',
        name: 'Range Rover',
        price: '150 million'
        },
        {
        productId: 8,
        imageLink: require("../assets/powerbike.jpg"),
        imageLink1: require("../assets/powerbike.jpg"),
        imageLink2: require("../assets/powerbike.jpg"),
        imageLink3: require("../assets/powerbike.jpg"),
        Description: 'It has no limits unlike cars',
        name: 'Power Bike',
        price: '15 million'
        },
        {
        productId: 9,
        imageLink: require("../assets/flying.jpg"),
        imageLink1: require("../assets/flying.jpg"),
        imageLink2: require("../assets/flying.jpg"),
        imageLink3: require("../assets/flying.jpg"),
        Description: 'It has zooming device of 10km away',
        name: 'Flying Spur',
        price: '350 million'  
        },
         {
        productId: 10,
        imageLink: require("../assets/benz.jpg"),
        imageLink1: require("../assets/benz.jpg"),
        imageLink2: require("../assets/benz.jpg"),
        imageLink3: require("../assets/benz.jpg"),
        Description: 'High speed with comfortable wheels',
        name: 'Mercedees benz c300',
        price: '75.7 million'
        },
        {
        productId: 11,
        imageLink: require("../assets/suzukibrezza.jpg"),
        imageLink1: require("../assets/suzukibrezza.jpg"),
        imageLink2: require("../assets/suzukibrezza.jpg"),
        imageLink3: require("../assets/suzukibrezza.jpg"),
        Description: 'Powerfull engine with less consuming fuel',
        name: 'Suzuki Brezza',
        price: '25.9 million'
        },
    ]
     
   }
  }
 }
</script>
<style scoped>
.pro{
     display: inline-block;
    margin: 5px;
}
#second{
   display: inline;
  }
  .boo{
     background-color: #f68b1e;
    width: 200%;
    height: 42px;
    margin: 0 auto;
    display: block;

  }
  #small{
    margin-top: 20px;
  }
  #space{
    padding: 20px;
  }
</style>

