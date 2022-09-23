<template>
  <Banner />
  <div class="main-container">
    <h1>Monte o seu burguer:</h1>
    <BurguerForm/>
     
  </div>
</template>

<script>
import Banner from '../components/banner.vue';
import BurguerForm from '@/components/BurguerForm.vue';

export default {
    name: "home",
    components: { Banner, BurguerForm },
   
}
</script>


<style scoped>
 h1{
  max-width: 500px;
  background-color: #FCBA03;
  margin: 0 auto;
  padding: 10px 20px;
  border-radius: 4px;
  font-size: 30px;
  margin-bottom: 10px;
 }
</style>

