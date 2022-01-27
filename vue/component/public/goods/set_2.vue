<template>
  <div class="border border-100 bg-white goods-default-style goods-set-1">
    <a  :href="'https://www.hawooo.com/mobile/product.aspx'+GoodsLink">
      <div class="goods-top p-2">
        <img class="img-fluid w-100 lazyautosizes lazyloaded" :src="'https://p8r7m4d5.stackpathcdn.com/images//' + GoodsImg" alt="Goods Logo" />
      </div>
        <div class="goods-bottom px-2 pb-3">
        <div class="goods-block  text-center justify-content-center py-2">
          <h6 class="goods-price mr-2">RM {{ GoodsPrice }}</h6>
          <span class="px-2 badge-pill badge-outline-primary hw-fs-12 discount-tag">
            {{ GoodsPrice }}
          </span>
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
      GoodsLink: [],
    },
  };
</script>
