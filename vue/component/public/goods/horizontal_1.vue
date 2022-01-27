<template>
  <div class="goods-horizontal-item">
    <a :href="'https://www.hawooo.com/mobile/product.aspx'+GoodsLink" class="p-3 row no-gutters">
      <div class="col-5">
        <img  class="img-fluid w-100 lazyautosizes lazyloaded" :src="'https://p8r7m4d5.stackpathcdn.com/images//' + GoodsImg">
      </div>
      <div class="col-7 p-3 d-flex align-content-between flex-wrap">
        <h6 class="mb-2  hw-fs-14 text-900 goods-neme">{{ GoodsName }}</h6>
        <h2 class="d-flex align-items-center hw-fs-16 text-primary mb-0">
          RM 84.90
          <span class="ml-2 hw-fs-13 text-600">{{ GoodsDiscount }}</span>
        </h2>
      </div>
    </a>
  </div>
</template>

<script>
  module.exports = {
    props: {
      GoodsImg: [],
      GoodsName: [],
      GoodsPrice: [],
      GoodsDiscount: [],
      BrandLogo: [],
      GoodsLink: [],
      isClicked: false,
    },
  };

</script>