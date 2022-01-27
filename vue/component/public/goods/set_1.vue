<template>
  <div class="border border-100 bg-white goods-default-style goods-set-1">
    <a class="goods-top" :href="'https://www.hawooo.com/mobile/product.aspx'+GoodsLink">

      <img class="img-fluid w-100 lazyautosizes lazyloaded" :src="'https://p8r7m4d5.stackpathcdn.com/images//' + GoodsImg" alt="Goods Logo" />
    </a>
    <div class="goods-bottom px-2 pt-2 pb-3">

      <div class="goods-block">
        <p class="goods-name"> {{ GoodsName }} </p>
      </div>
      <div class="goods-block">
        <h6 class="goods-price">RM {{ GoodsPrice }}</h6>
      </div>
    </div>
  </div>
</template>

<script>
  module.exports = {
    props: {
      GoodsImg: [],
      GoodsName: [],
      GoodsPrice: [],
      GoodsLink: [],
    },
  };

</script>