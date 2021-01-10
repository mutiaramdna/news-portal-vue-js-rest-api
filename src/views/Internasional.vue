<template>
  <div class="internasional">
    <Navbar />
    <div class="container">
      <Hero />
      <div class="row mb-3">


        <div class="col-md-4 mt-4" v-for="(content, index) in contents" :key="index">
          <Kartu :content="content" />
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
  name: "Internasional",
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
      .get("http://localhost:8081/internasional")
      .then((response) => this.setContent(response.data.data))
      .catch(function (error) {
        // handle error
        console.log("gagal ndes");
        console.log(error);
      })
      .then(function () {
        // always executed
      });
  },
};
</script>