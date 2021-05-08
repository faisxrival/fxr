<template>
  <div class="product">
    <HeaderFxr />

    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more text-left">
                        <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="gambar_default" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider" :dots="false" :nav="false">
                                    <div class="pt" @click="changeImage(thumbs[0])" :class="thumbs[0] == gambar_default ? 'active' : ''">
                                        <img src="img/products/dropdead/dropdead-chopper1.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[1])" :class="thumbs[1] == gambar_default ? 'active' : ''">
                                        <img src="img/products/dropdead/dropdead-chopper2.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[2])" :class="thumbs[2] == gambar_default ? 'active' : ''">
                                        <img src="img/products/dropdead/dropdead-chopper3.jpg" alt="" />
                                    </div>

                                    <div class="pt" @click="changeImage(thumbs[3])" :class="thumbs[3] == gambar_default ? 'active' : ''">
                                        <img src="img/products/dropdead/dropdead-chopper4.jpg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details text-left">
                                <div class="pd-title">
                                    <span>Hoodie</span>
                                    <h3>Dropdead Chopper</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Description
                                    </p>
                                    <p>
                                        Long-sleeve, relaxed fit cotton hoodie in black with a cropped hem. Featuring large printed graphics at the front in white and red. Kangaroo pocket at the front. Tonal Stitching.<br/>
                                        • Joe is 6ft and wearing a size L<br/>
                                        • 100% Cotton<br/>
                                        • This item is machine washable at 30<br/>
                                    </p>
                                    <h4>£80.00</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="/cart"><a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a></router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

    <RelatedFxr />
    <FooterFxr />
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import HeaderFxr from '@/components/HeaderFxr.vue';
import FooterFxr from '@/components/FooterFxr.vue';
import RelatedFxr from '@/components/RelatedFxr.vue';
import carousel from 'vue-owl-carousel';


export default {
    name: 'Product',
    components: {
        HeaderFxr,
        FooterFxr,
        RelatedFxr,
        carousel
    },
    data() {
        return {
          gambar_default: "img/products/dropdead/dropdead-chopper1.jpg",
          thumbs: [
                "img/products/dropdead/dropdead-chopper1.jpg",
                "img/products/dropdead/dropdead-chopper2.jpg",
                "img/products/dropdead/dropdead-chopper3.jpg",
                "img/products/dropdead/dropdead-chopper4.jpg",
          ]
        }
    },
    methods: {
        changeImage(urlImage) {
            this.gambar_default = urlImage;
        }
    } 
}
</script>

<style scoped>
.product-thumbs .pt {
    margin-right: 15px;
}
</style>