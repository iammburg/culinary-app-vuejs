<template>
  <div class="home">
    <NavBar />
    <div class="container">
      <HeroSection />

      <div class="row mt-4">
        <div class="col">
          <h2>Best <strong>Foods</strong></h2>
        </div>
        <div class="col">
          <router-link
            to="/foods"
            class="btn btn-success float-right"
            ><b-icon-eye></b-icon-eye> See All</router-link
          >
        </div>
      </div>

      <div class="row mb-4">
        <div
          class="col-md-4 mt-4"
          v-for="product in products"
          :key="product.id">
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/Navbar.vue";
import HeroSection from "@/components/Hero.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "HomeView",
  components: {
    NavBar,
    HeroSection,
    CardProduct,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    // Make a request for a user with a given ID
    axios
      .get("http://localhost:3000/best-products")
      .then((response) => {
        // handle success
        // console.log("Berhasil: ", response);
        this.setProduct(response.data);
      })
      .catch((error) => {
        // handle error
        console.log("Gagal", error);
      });
  },
};
</script>
