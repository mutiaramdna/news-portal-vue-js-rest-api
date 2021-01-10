<template>
  <div>
    <Navbar />
    <h2>Ini {{ $route.params.link }}</h2>
    <p>Jebal {{ baca.judul }}</p>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import axios from "axios";
export default {
  name: "Detail",
  components: {
    Navbar,
  },
  data() {
    return {
      bacas: [],

    };
  },
  methods: {
    setBaca(data) {
      this.bacas = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:8081/detail/?url="+ this.$route.params.link)
      .then((response) => this.setBaca(response.data.data))
      .catch(function (error) {
        // handle error
        console.log(error);
      })
  },
};
</script>

<style>
</style>