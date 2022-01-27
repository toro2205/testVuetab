<template>

  <div class="border border-250 p-2 pb-5 goods-default-style">
    <a :href="'https://www.hawooo.com/mobile/product.aspx'+GoodsLink">
      <div class="position-relative">
        <div class="p-2">
          <img :src="'https://p8r7m4d5.stackpathcdn.com/images//' + GoodsImg"  class="img-fluid" />
        </div>
        <div class="position-absolute b-0 l-0 r-0 brand-logo text-center" style="transform:translateY(25px)">
          <img :src="'https://www.hawooo.com/images/' + BrandLogo" class="img-fluid mx-auto bg-white border border-200 shadow-sm" />
        </div>
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
    },

  };

</script>