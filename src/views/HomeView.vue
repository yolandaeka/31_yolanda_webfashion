<template>
 <div class="home">

  <v-carousel hide-delimiters
  height="465">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >


    <v-row  
    align="center"
    justify="center"
    style="height: 470px;"
    no-gutters
    wrap>

    <v-card
    color="transparent"
    elevation="0"
    align="center"
    >

    <v-card-text class="series-change white--text text-center">Elizabeth Series</v-card-text>
    
    <v-btn 
    class= "btn-change white--text "
        color="#D9B285"
        elevation="3"
    >  SEE COLLECTION 
    </v-btn>
    
        </v-card>
      </v-row>
    </v-carousel-item>
  </v-carousel>

  <v-spacer></v-spacer>

  <!-- latest section -->

<v-container >
   <v-card-title class="title-card"> LATEST
    <v-spacer></v-spacer>
    <v-btn
    text
    class="black--text">
        SEE ALL
      </v-btn>
  </v-card-title>
  
  
  <v-row
    align="center"
    justify="center"
    >
    <v-col
      v-for="(product,i) in products"
      :key="i"
      >

  <v-card
    max-width="216"
    class="mx-auto"
    justify="center"
    
  >

    <v-img
      :src="product.image" width="216" height="320"
    ></v-img>

    <v-card-title class="card-latest">{{product.name}}</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>
    
    </v-card-text>

      <v-card-text color="#EB801E" class="price" >
          {{ product.price }}
        </v-card-text>

      <v-spacer></v-spacer>

    <v-card-actions>
      <v-btn
      
        color="#D9B285"
        @click="reserve"
        class="white--text mt-5"
        block
        elevation="5"
      >
       ADD TO CART
      </v-btn>
    </v-card-actions>
  </v-card>

</v-col>
  </v-row>
</v-container>

<v-spacer></v-spacer>
  

  <!-- POPULAR SECTION -->
<v-container  mb-10>
  <v-card-title class="title-card">POPULAR
    <v-spacer></v-spacer>
    <v-btn
    text
    class="black--text">
        SEE ALL
      </v-btn>
  </v-card-title>

  <v-row
    align="center"
    justify="center"
    >
    <v-col
      v-for="(product,i) in products"
      :key="i"
      >

  <v-card
    max-width="216"
    class="mx-auto"
    justify="center"
    
  >

    <v-img
      :src="product.image" width="216" height="320"
    ></v-img>

    <v-card-title class="card-latest">{{product.name}}</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>
    
    </v-card-text>

      <v-card-text color="#EB801E" class="price" >
          {{ product.price }}
        </v-card-text>

      <!-- <v-spacer></v-spacer> -->

    <v-card-actions>
      <v-btn
      
        color="#D9B285"
        @click="reserve"
        class="white--text mt-5"
        block
        elevation="5"
      >
       ADD TO CART
      </v-btn>
    </v-card-actions>
  </v-card>

</v-col>
  </v-row>
  
  </v-container>


  <!-- ABOUT SECTION -->

<v-spacer></v-spacer>

  

  <v-img
   src="../assets/imghome/image 4.png">
   <v-row 
    no-gutters
    justify="center"
    align="center"
    style="height: 437px;"
    >
    <v-col>

 <v-card
    color="transparent"
    elevation="0"
    align="center"
    >
  <h2 class="white--text">ABOUT US</h2>

    <v-card-text class="about white--text" width="100" height="144" >Lorem ipsum dolor sit amet, 
      consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna 
      aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip 
      ex ea commodo consequat. Duis aute irure dolor in reprehenderit in 
      voluptate velit esse cillum dolore eu fugiat nulla pariatur.</v-card-text>
    
    <v-btn 
    class= "btn-change white--text "
        color="#D9B285"
        elevation="3"
    >  LEARN MORE 
    </v-btn>
    
    </v-card>
     </v-col>
</v-row>
  </v-img>
 


<!-- rating section -->

<v-container>

  <v-card-title class="title-card text-center justify-center mt-5 mb-4"> TESTIMONIALS</v-card-title>
  <v-row 
  
    >
    

    <v-col
    v-for="(testimonial,i) in testimonials"
    :key="i">
      <v-card
    max-width="374"
    color="#F0DCC5"
    
  >
 
   <v-card-actions>
      <v-list-item class="grow">
        <v-list-item-avatar>
          <v-img
            class="elevation-6"
            alt=""
            :src="testimonial.image"
          ></v-img>
        </v-list-item-avatar>

        <v-list-item-content >
          <v-list-item-title>{{testimonial.name}}</v-list-item-title>
           <v-card-text>
      <v-row>
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="13"
        ></v-rating>
      </v-row>
      </v-card-text>
        </v-list-item-content>
      </v-list-item>
         </v-card-actions>

      <v-card-text class="text-testi black--text pt-0" width="100" height="145" > {{ testimonial.testi }} </v-card-text>
   
  </v-card>

    </v-col>

  </v-row>

</v-container >

<v-container class="mt-5 mb-8">

<p class="title-card text-center mt-7"> BUAT KIRIMAN BARU</p>
 <p class="text-caption text-center mb-4">Setiap kiriman yang ditambahkan akan ditampilkan pada halaman depan.</p>

<form class="mt-5">
    <v-text-field
      v-model="name"
      :error-messages="nameErrors"
      :counter="10"
      label="Name"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>
    <v-text-field
      v-model="email"
      :error-messages="emailErrors"
      label="E-mail"
      required
      @input="$v.email.$touch()"
      @blur="$v.email.$touch()"
    ></v-text-field>

    <v-text-field
      v-model="testo"
      label="Testimoni"
      required
    ></v-text-field>

    <p class="label mt-5">Tap to rate</p>   

    <v-rating
      v-model="rating"
      background-color="#F0DCC5"
      color="#F0DCC5"
      size="36">

    </v-rating>



    <v-checkbox
      v-model="checkbox"
      :error-messages="checkboxErrors"
      label="Do you agree?"
      required
      @change="$v.checkbox.$touch()"
      @blur="$v.checkbox.$touch()"
    ></v-checkbox>

    <v-btn
      class="mr-4"
      @click="submit"
    >
      submit
    </v-btn>
    <v-btn @click="clear">
      clear
    </v-btn>
  </form>

  </v-container>

<!-- footer -->

<v-footer
    padless
  >
    <v-card
      flat
      tile
      class=" white--text text-center mt-15"
      color="#D9B285"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>DOROTHEA</strong>
      </v-card-text>
    </v-card>
  </v-footer>



</div>
</template>



<script>

// eslint-disable-next-line no-unused-vars


export default {
  
    data () {
      return {
      items: [
        {
          src: require('../assets/imghome/webphoto (1).png')
        },
        {
          src: require('../assets/imghome/webphoto (2).png')
        },
        {
          src: require('../assets/imghome/webphoto (3).png')
        }
      ],

      products: [
        {
        image: "https://i.pinimg.com/564x/99/12/22/991222ca391c945718feab5ffa47f359.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 150.000"

        },

        {

        image: "https://i.pinimg.com/564x/24/f7/af/24f7affc7e3c13e2e498fc3c63dc1f49.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 160.000"
        },

        {
        image: "https://i.pinimg.com/564x/f1/d7/e6/f1d7e6be9189157868fe81507a3e90b5.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 90.000"
        },

        {
        image: "https://i.pinimg.com/564x/67/21/3c/67213c8f543a2081c2ff3bd69c02beb3.jpg",
        name : "Green Plaid Long Skirt from Elizabeth Series",
        price : "Rp 250.000"

        }

      ],

      testimonials: [
        {
          image: "https://i.pinimg.com/564x/ba/d4/1d/bad41dcc814d7f456fec53d4554995f3.jpg",
          name: "Bae Irene",
          testi: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },

        {
          image: "https://i.pinimg.com/564x/62/e2/db/62e2dbf2b5e487900e51b4d9aef61881.jpg",
          name: "Edward Ryan",
          testi: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },

        {
          image: "https://i.pinimg.com/564x/53/19/a1/5319a1e5af41a11770da19008d84ba76.jpg",
          name: "Aisha Kim",
          testi: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        }

      ],
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ]
      }  
}
}
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@700&family=Montserrat:wght@500;600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');

.btn-change{
  font-family:'Montserrat', sans-serif;
  font-size: 14px;
}

.series-change{
   font-family: 'Merriweather',serif;
   font-size: 22px;
   letter-spacing: 5px;
   font-weight: 700;
}


.title-card{
  font-family:'Montserrat', sans-serif;
  font-weight: 700;
  font-size: 20px;


}

.card-latest{
  font-family: 'Merriweather',serif;
   font-size: 13px;
   line-height: 24px;
  
}

.price{
  font-size: 17px;
}

.about{
  font-family:'Montserrat', sans-serif;
  font-weight:500;
  font-size: 15px;
  text-align: center;
  width:900px;
}

.text-testi{
  font-family: 'Montserrat', sans-serif;
  font-size: 15px;
  font-weight:500;
  text-align: center;
}



</style>
