<template>
  <div class="detail-swiper">
    <swiper class="swiper1">
        <swiper-item v-for="(item,index) in topImages" :key="index">
            <img :src="item" alt />
        </swiper-item>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperItem } from "components/common/swiper/index";
export default {
  props: {
    topImages: {
      type: Array,
      default() {
        return [];
      }
    }
  },
  components: {
    Swiper,
    SwiperItem
  }
};
</script>

<style scoped>
.swiper1{
    height: 300px;
    overflow:hidden;
}
/* .swiper1 img{
    height:300px;
} */
</style>