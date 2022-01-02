<template>

  <div class="container">
    <div class="row">
      <div class="col-lg-7 my-3 p-3">
        <div class="text-center">
          <h1>麵風屋 Ramen</h1>
          <img alt="Vue logo" src="./assets/ramen.png" id="ramen-logo">
          <p class="mt-3 align-self-end">台北市信義區松麵路一段5號</p>

          <div class="btn btn-primary mt-5
            animate__bounce animate__infinite"
            :class="{
              animate__animated: smile !== '😀'
            }"
            @mouseover="smile = '😀'"
            @mouseleave="smile = ''" >下麵 {{ smile }}</div>
        </div>
      </div>
      <div class="col-lg-5 mx-auto my-3 p-3 rounded border border-info">
        <Ramen/>
      </div>
    </div>
  </div>
</template>

<script>
import Ramen from './components/Ramen.vue'

export default {
  name: 'App',
  data(){
    return {
      smile: ''
    }
  },
  components: {
    Ramen
  }
}
</script>

<style>
@import'~bootstrap/dist/css/bootstrap.css';
@import '~animate.css/animate.css';
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@100;300;400;500;700;900&display=swap');

#ramen-logo{
  width: 150px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 30px;
  font-family: 'Noto Sans TC', sans-serif;
}
</style>
