<template>

    <div class="small-slider_container">

        <div class="sale-block">
            <span class="sale">Распродажа</span>
        </div>

        <div class="small-slider">

            <swiper :options="swiperOption" ref="mySwiper">

                <swiper-slide  v-for="(product, id) in products" :key="id">
                    <product-card-component :item="product"/>
                </swiper-slide>


                <!--<div class="swiper-button-prev" slot="button-prev">-->
                    <!--&lt;!&ndash;<img src="images/left-arrow_active.png"/>&ndash;&gt;-->
                <!--</div>-->

                <!--<div class="swiper-button-next" slot="button-next">-->
                    <!--&lt;!&ndash;<img src="images/right-arrow_active.png"/>&ndash;&gt;-->

                <!--</div>-->
            </swiper>
        </div>
    </div>

</template>

<script>
    import 'swiper/dist/css/swiper.css'

    import {swiper, swiperSlide} from 'vue-awesome-swiper'
    import ProductCardComponent from "./ProductCardComponent";
    export default {
        name: "SmallSliderComponent",
        data() {
            return {
                products: [
                    {
                        id: 1,
                        img: 'images_secur/Layer 36.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },

                    {
                        id: 4,
                        img: 'images_secur/Layer 83.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },

                    {
                        id: 7,
                        img: 'images_secur/Layer 86.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },

                    {
                        id: 10,
                        img: 'images_secur/Layer 80.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },
                    {
                        id: 1,
                        img: 'images_secur/Layer 36.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },


                ],
                swiperOption: {
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    },
                    slidesPerView: 1,
                    setWrapperSize: true,
                    grabCursor: true,
                }
            }
        },

        components: {
            ProductCardComponent,
            swiper,
            swiperSlide
        }

    }
</script>

<style>
    .small-slider_container {
        width: 100%;
        max-width: 290px;
        min-height: 369px;
        border-radius: 30px;
        background-image: url('~@/assets/Vector Smart Object.png');
    }
    .sale-block {
        width: 121px;
        height: 31px;
        border-radius: 16px;
        background-color: #ffd333;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        margin-left: 20px;
        margin-top: 20px;
    }
    .sale {
        color: #000000;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 500;
        line-height: 14px;
        text-transform: uppercase;
        letter-spacing: 0.17px;
    }
    .small-slider {
        margin-top: 30px;
    }


    @media (min-width: 1200px) {
        .small-slider_container {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-orient: vertical;
            -webkit-box-direction: normal;
            -ms-flex-direction: column;
            flex-direction: column;
        }

    }
    @media (max-width: 1024px){
        .small-slider_container {
            display: none;
        }
    }

</style>