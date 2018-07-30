<template>
    <div>
      <div style="color: #494949; font-size: 5rem;
                  font-weight: bolder; text-align: center; margin-top: 10vh;">TokenSale</div>
      <div style="position: relative">
        <parallax :fixed="true">
          <img src="../static/img/image2.jpg">
        </parallax>
      </div>
          <!-- Router-view -->
          <nuxt/>
          <!-- Router-view -->
    </div>
</template>

<script>
  import Parallax from 'vue-parallaxy'
  export default {
    name: 'TokenSale',
    components: {
      Parallax
    }
  }
</script>

<style>

</style>
