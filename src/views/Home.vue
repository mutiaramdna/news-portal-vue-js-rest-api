<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />
      <div class="row mb-3">
        <div class="col-md-4 mt-4">
          <Kartu />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Hero from "../components/Hero.vue";
// @ is an alias to /src

import Navbar from "../components/Navbar.vue";
import Kartu from "../components/Kartu.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    Kartu,
  },
  data() {
    return {
      contents: [],
    };
  },
  methods: {
    setContent(data) {
      this.contents = data;
    },
  },
  mounted() {
    

    // Make a request for a user with a given ID
    axios
      .get("http://localhost:8081/#")
      .then(function (response) {
        // handle success
        console.log("mantap");
        console.log(response.data);
      })
      .catch(function (error) {
        // handle error
        console.log('gagal ndes');
        console.log(error);
      })
      .then(function () {
        // always executed
      });
  },
};
</script>
