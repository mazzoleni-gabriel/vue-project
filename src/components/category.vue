<template>
    <div class="slider">
        <h3>{{categoryName}}</h3>      
        <span v-on:mouseover="scrollLeft()" v-on:mouseout="clearScroll()" class="handle handlePrev active">
            <i class="fa fa-caret-left" aria-hidden="true"></i>
        </span>

        <div ref="scroller" class="row">
            <div class="row__inner">
                <movie name="Pantera negra" description="asdasdasdasd"  image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" description="asdasdasdasd"  image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
                <movie name="Pantera negra" image="https://boygeniusreport.files.wordpress.com/2018/04/black-panther.jpg?quality=98&strip=all&w=1200"></movie>
            </div>
        </div>

        <span v-on:mouseover="scrollRight()" v-on:mouseout="clearScroll()" class="handle handleNext active">
            <i class="fa fa-caret-right" aria-hidden="true"></i>
        </span>
    </div>
</template>

<script>

import movie from './movie.vue';

export default {
  props: ["categoryName"],
  data() {
    return {
      appName: "Netflix de Pobre",
      interval: null
    };
  },
  components: {
      movie
  },
  methods: {
    scrollRight() {
      this.interval = setInterval(() => {
        this.$refs.scroller.scrollLeft += 1;
      }, 5);
    },
    scrollLeft() {
      this.interval = setInterval(() => {
        this.$refs.scroller.scrollLeft -= 1;
      }, 5);
    },
    clearScroll() {
      clearInterval(this.interval);
    }
  }
};
</script>

<style lang="scss">
</style>

