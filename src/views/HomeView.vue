<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="header">
        <v-row>
          <v-col cols="5">
            <br><br>
            <div style="position: relative;" class="mt-16">
              <h1 class="text-white">Welcome to Ananas</h1>
              <span class="text-white">Shoes, Sandals and more</span><br>
              <v-btn tile dark class="text-red mt-8" variant="outlined">Buy Now</v-btn>
            </div>
          </v-col>
          <v-col cols="2">

          </v-col>
          <v-col cols="5">
            <div style="position: relative;z-index: 999;" class="mt-16">
              <v-img src="welcome.png" contain max-height="300px"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
            <div class="us_img">
              <br><br>
              <v-img src="us.png" max-height="250px"></v-img>
            </div>
          </v-col>
          <v-col cols="12" sm="6">
            <h2 class="mt-16">About Us</h2>
            <h3 class="mt-2">Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Quisquam, mollitia temporibus!</h3>
            <h4 class="mt-2">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Numquam
              possimus eaque dignissimos, voluptas quia ipsum. Ducimus, placeat possimus eius aliquid id sed facere totam,
              tenetur fugit saepe distinctio quos? Animi, quod vero neque optio temporibus architecto nisi distinctio
              aliquam quia!</h4>
            <h4  class="mt-2">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veniam
              sunt reprehenderit, magnam officiis aut eaque consectetur exercitationem nisi quia. Ea.</h4>
            <v-btn tile dark color="yellow" class="mt-4">Shop Now</v-btn>
          </v-col>
          </v-row>
        </div>
      </v-col>
      <v-divider></v-divider>
      <!-- shopping list -->
      <div class="text-center mt-12">
        <h2>Shopping List</h2>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                icon=""
                  color="yellow"
                  class="text-dark"
                ><i class="fa-solid fa-laptop"></i></v-btn>
                <h3 class="ml-3 mt-4">Laptop</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem, ipsum dolor sit amet <br />consectetur adipisicing
                  <br />consectetur adipis
                </p>
              </div>
              <div class="child">
                <v-btn
                icon
                  color="yellow"
                  class="text-dark"
                ><i class="fa-solid fa-mobile-screen-button"></i></v-btn>
                <h3 class="ml-3 mt-4">Phone</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem, ipsum dolor sit amet <br />consectetur adipisicing
                  <br />consectetur adipis
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon=""
                  color="yellow"
                  class="text-dark"
                ><i class="fa-solid fa-camera"></i></v-btn>
                <h3 class="ml-3 mt-4">Camera</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem, ipsum dolor sit amet <br />consectetur adipisicing
                  <br />consectetur adipis
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <!-- End shopping list -->
      <!-- Product -->
      <v-col cols="12" sm="12" id="service">
        <div class="d-flex justify-center mb-6">
          <v-btn color="yellow" class="mr-5">All Product</v-btn>
          <v-btn variant="tonal" class="mr-5">Hot Deals</v-btn>
          <v-btn variant="tonal" class="mr-5">Laptops</v-btn>
          <v-btn variant="tonal" class="mr-5">Phones</v-btn>
          <v-btn variant="tonal">Camera</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="product_img">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :key="{'on-hover' : isHovering}" v-bind="props">
                  <v-img :src="item.img" height="200px" cover></v-img>
                  <v-btn v-show="isHovering" class="view_more_btn">View More</v-btn>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="yellow" class="mt-5">More</v-btn>
        </div>
        <v-divider></v-divider>
      </v-col>
      
      <!-- End Product -->

      <!-- Page -->
      <v-col cols="12" id="page">
        <div class="page_content">
          <v-row>
            <v-col cols="12" sm="4">
            <v-card class="mr-auto" max-width="350px" height="">
              <v-img src="hinh2.jpg" height="200px" cover></v-img>
              <v-card-title>Lorem ipsum dolor sit amet.</v-card-title>
              <v-card-subtitle>Lorem ipsum dolor sit amet.</v-card-subtitle>
              <v-card-text>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat velit quas cum! A quasi consectetur veniam autem iusto incidunt hic.
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="mr-auto" max-width="350px" height="">
              <v-img src="hinh2.jpg" height="200px" cover></v-img>
              <v-card-title>Lorem ipsum dolor sit amet.</v-card-title>
              <v-card-subtitle>Lorem ipsum dolor sit amet.</v-card-subtitle>
              <v-card-text>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat velit quas cum! A quasi consectetur veniam autem iusto incidunt hic.
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="mr-auto" max-width="350px" height="">
              <v-img src="hinh2.jpg" height="200px" cover></v-img>
              <v-card-title>Lorem ipsum dolor sit amet.</v-card-title>
              <v-card-subtitle>Lorem ipsum dolor sit amet.</v-card-subtitle>
              <v-card-text>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat velit quas cum! A quasi consectetur veniam autem iusto incidunt hic.
              </v-card-text>
            </v-card>
          </v-col>
          </v-row>
        </div>
      </v-col>
      <!-- End Page -->
      <!-- Contact -->
      <v-divider></v-divider>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <h2 class="mt-8">Give us feedback</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, perferendis et itaque, libero, repellat aspernatur totam inventore maiores nulla odit tenetur corrupti. Facilis, quae earum quod voluptas eligendi voluptate ullam?
        </p>
        <v-row class="mt-8">
          <v-col cols="12" sm="5">
            <v-text-field label="Name" hint="" variant="outlined"></v-text-field>
          </v-col>
          <v-col cols="12" sm="7">
            <v-text-field label="Email" hint="" variant="outlined"></v-text-field>
          </v-col>
        </v-row>
        <v-textarea label="Feedback" hint="" variant="outlined"></v-textarea>
        <v-btn  color="yellow" class="mt-1">Submit</v-btn>
      </v-col>
      <v-divider></v-divider>
      <!-- End Contact -->
    </v-container>
    <Footer />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '../components/NavBar.vue'
import Footer from '../components/Footer.vue'

export default defineComponent({
  name: 'HomeView',

  setup(){
    return{
      items:[
        {
          img: "l1.jpg",
        },
        {
          img: "l2.jpg",
        },
        {
          img: "l3.jpg",
        },
        {
          img: "c1.jpg",
        },
        {
          img: "c2.jpg",
        },
        {
          img: "c3.jpg",
        },
        {
          img: "p1.jpg",
        },
        {
          img: "p2.jpg",
        },
        {
          img: "p3.jpg",
        },
      ],
    };
  },

  components: {
    NavBar,
    Footer,
  },
});
</script>
<style>

.view_more_btn {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
  font-size: 18px;
  background-color: yellow;
  color: white;
  padding: 10px 20px;
  border-radius: 4px;
}

.v-card__text:hover {
  opacity: 0.7;
}


.page_content{
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: gainsboro;

}


.product_img {
  padding: 0 200px;
}

.first{
  width: 100%;
  height: 300px;
  text-align: center;
  padding: 32px 32px;
}

.child{
  display: inline-block;
  padding: 32px 16px;
  vertical-align: center;
  margin-right: 10px;
}

.us_img {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 370px;
  height: 340px;
  background-color: aqua;
  border-radius: 50%;
}

.v-container {
  padding: 16px 0 16px 0;
}

.header {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.header:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 5deg);
}

.header:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -5deg);
}</style>
