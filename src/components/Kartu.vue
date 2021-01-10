<template>
  <div>
    
    <div class="card shadow mt-1">
      <b-card>
        <b-card-text>
          <img :src="content.poster" height="180" width="310">
          <h4>{{ content.judul }}</h4>
          <b-button variant="primary" :href="content.link" target="_blank">Read more...</b-button>
          <!--<router-link class="btn btn-success" :to="'/detail/?url='+content.link"><b-icon-book></b-icon-book> Read more..</router-link>-->
          <!--<router-link :to="{name: 'Detail', params: { link: content.link }}" class="btn btn-success">Read more..</router-link>-->
          <p>{{ content.waktu }}</p>
        </b-card-text>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "Kartu",
  props: ["content"],
};
</script>

<style>
</style>