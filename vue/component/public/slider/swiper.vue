<template id="swiper">
  <!-- Swiper -->
  <div class="swiper-container hw-swiper-container  overflow-hidden">

    <!-- Add Arrows -->
    <slot name="hw-swiper-arrows">
    </slot>


    <ul class="swiper-wrapper">
      <!--頁面放置Swiper內容-->
      <slot></slot>
    </ul>

    <!-- Add Pagination -->
    <slot class="swiper-pagination" name="swiper-pagination">
    </slot>
    <!--<div class="swiper-pagination"></div>-->
  </div>
</template>

<script>
  module.exports = {
    mounted() {
      new Swiper(this.$el, {
        slidesPerView: +this.perview,
        spaceBetween: +this.space,
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
          //type: 'fraction',
        },
        navigation: {
          nextEl: '.hw-swiper-next',
          prevEl: '.hw-swiper-prev',
        },
        //breakpoints: {
        //  650: {
        //    slidesPerView: 2,
        //    centeredSlides: false,
        //    spaceBetween: 10,
        //  },
        //}
      });
    },
    props: {
      perview: {
        //type: Number,
        default: 1
      },
      space: {
        type: Number,
        default: 2
      },
    },
  };
</script>