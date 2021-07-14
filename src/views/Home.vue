<template>
  <div id="homepage-container">
    <div class="grid-container">
      <div id="carousel-container">
      <v-carousel
        touchless
        height="inherit"
        hide-delimiters
        :show-arrows="false"
        cycle
        interval="3000"
      >
        <v-carousel-item
          v-for="(item, i) in carouselItems"
          :key="i"
          :src="item"
          transition="fade-transition"
        >
        </v-carousel-item>
      </v-carousel>
      </div>
      <v-card class="service-card" to="/shop" dark>
        <v-img :src="localesImage" position="top" max-height="500"></v-img>
        <v-card-title>Frutas y Vegetales</v-card-title>
        <v-card-subtitle style="text-align: left"
          >Frutas y vegetales frescos directamente de granjas y agricultores
          locales</v-card-subtitle
        >
      </v-card>
      <v-card class="service-card" dark>
        <v-img :src="deliveryTruck"></v-img>

        <v-card-title>Servicio a Domicilio</v-card-title>
        <v-card-subtitle style="text-align: left"
          >Free Delivery on Thursdays and Saturdays</v-card-subtitle
        >
      </v-card>
      <v-card class="service-card" dark>
        <v-img :src="restaurantImage" max-height="500"></v-img>
        <v-card-title>Para Restaurantes</v-card-title>
        <v-card-subtitle style="text-align: left"
          >Servicio personalizado para restaurantes con compras programables
          semanal o mensualmente.</v-card-subtitle
        >
      </v-card>

    </div>
  </div>
</template>

<script>
import deliveryTruck from "@/assets/images/delivery-truck.jpeg";
import restaurantImage from "@/assets/images/restaurant.jpeg";
import fruits from "@/assets/images/fruits.jpg";
import veggies from "@/assets/images/veggies.jpg";
import delivery from "@/assets/images/delivery.jpg";
import locales from "@/assets/images/locales.jpeg";

// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  data() {
    return {
      carouselItems: [fruits, veggies, delivery],
      localesImage: locales,
      restaurantImage: restaurantImage,
      deliveryTruck: deliveryTruck
    };
  },
};
</script>


<style scoped>

.grid-container {
  margin: 0 auto !important;
}

#carousel-container {
  width: 100vw;
  height: 300px;
  max-width: 1200px;
}

.service-icon {
  font-size: 4rem !important;
  margin: 2rem;
  color: #159c84 !important;
}

.service-card {
  width: 100vw;
  max-width: 500px;
  height: min-content;
  margin-top: 1rem;
}

@media (min-width: 900px) {

  #carousel-container {
    width: 100%;
    height: auto;
  }

  .service-card {
    margin: 0;
  }

  .grid-container {
    border: 1px dashed yellow;
    display: grid;
    
    grid-template-rows: min-content;
   grid-template-columns: 2fr 1fr; 
    gap: 1rem;
    width: max-content;
    padding: 3rem !important;
  }
}
</style>
