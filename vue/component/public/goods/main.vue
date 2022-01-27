<template>
  <div class="border border-100 bg-white goods-default-style goods-main">
    <a class="goods-top" :href="'https://www.hawooo.com/mobile/product.aspx'+GoodsLink">
      <div class="position-absolute live-free-shipping">
        <img src="images/icon/live_free_shipping.svg" class="img-fluid" />
      </div>
      <img class="img-fluid w-100 lazyautosizes lazyloaded" :src="'https://p8r7m4d5.stackpathcdn.com/images//' + GoodsImg" alt="Goods Logo" />
    </a>
    <div class="goods-bottom px-2 pt-2 pb-3">
      <div class="goods-block">
        <span class="mr-2 badge badge-lighter-secondary goods-tag">
          <img src="https://www.hawooo.com/images/icon/%E7%86%B1%E5%93%81.svg" />
          <span>Hot</span>
        </span>
      </div>
      <div class="goods-block">
        <p class="goods-name"> {{ GoodsName }} </p>
      </div>
      <div class="goods-block">
        <h6 class="goods-price">RM {{ GoodsPrice }}</h6>
      </div>
      <div class="goods-block">
        <!--<span class="text-500 font-weight-bold hw-fs-12 item-price"><del>RM 104.00</del></span>-->
        <span class="goods-discount"> {{ GoodsDiscount }}</span>
      </div>
      <div class="goods-block">
        <p class="goods-view"><i class="far am-icon-eye mr-1"></i>492.3K</p>
      </div>
      <!--Like Icon -->
      <div class="rounded-circle shadow-sm p-2 border border-250 goods-like-icon">
        <a value="button" :style="isClicked ? { 'color': '#EE5984' } : null" @click="getBrandCoupon()"><span class="material-icons">favorite</span></a>
      </div>
    </div>
  </div>
</template>

<script>
  module.exports = {
    props: {
      GoodsImg: [],
      GoodsName: [],
      GoodsPrice:[],
      GoodsDiscount: [],
      BrandLogo: [],
      GoodsLink: [],
      isClicked: false,
    },
    //sweetalert2
    methods: {
      getBrandCoupon: function () {
        this.isClicked = !this.isClicked
        const Toast = Swal.mixin({
          toast: true,
          position: 'bottom-center',
          showConfirmButton: false,
          timer: 2000,
          timerProgressBar: false,
          customClass: {
            popup: 'colored-toast'
          },
          didOpen: (toast) => {
            toast.addEventListener('mouseenter', Swal.stopTimer)
            toast.addEventListener('mouseleave', Swal.resumeTimer)
          }
        })

        Toast.fire({
          icon: 'success',
          title: 'Added to my favorites!'
        })
      }
    },

  };

</script>