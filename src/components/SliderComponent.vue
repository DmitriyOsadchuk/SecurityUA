<template>

    <div class="slider_container">
        <div class="slider-sort">
            <div class="button-top">
                <li class="top"><a href="#">Хиты продаж</a></li>
            </div>
            <li class="new"><a href="#">Новинки</a></li>
            <li class="action"><a href="#">Акции</a></li>
        </div>
        <div class="slider">
        <swiper :options="swiperOption" ref="mySwiper">
            <swiper-slide  v-for="(product, id) in products" :key="id">
                <product-card-component :item="product"/>
            </swiper-slide>
        </swiper>
        </div>
    </div>

</template>

<script>
    import 'swiper/dist/css/swiper.css'

    import {swiper, swiperSlide} from 'vue-awesome-swiper'
    import ProductCardComponent from "./ProductCardComponent";

    export default {
        name: "SliderComponent",
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
                        id: 2,
                        img: 'images_secur/Layer 39.png',
                        title: 'ВИДЕОКАМЕРА HAC-HDW120EMP-A-036B-S3',
                        price: '2.822'
                    },
                    {
                        id: 3,
                        img: 'images_secur/Layer 40.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '8.000'
                    }, {
                        id: 4,
                        img: 'images_secur/Layer 83.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },
                    {
                        id: 5,
                        img: 'images_secur/Layer 88.png',
                        title: 'ВИДЕОКАМЕРА HAC-HDW120EMP-A-036B-S3',
                        price: '2.822'
                    },
                    {
                        id: 6,
                        img: 'images_secur/Layer 85.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '8.000'
                    },
                    {
                        id: 7,
                        img: 'images_secur/Layer 86.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },
                    {
                        id: 8,
                        img: 'images_secur/Layer 87.png',
                        title: 'ВИДЕОКАМЕРА HAC-HDW120EMP-A-036B-S3',
                        price: '2.822'
                    },
                    {
                        id: 9,
                        img: 'images_secur/Layer 89.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '8.000'
                    },
                    {
                        id: 10,
                        img: 'images_secur/Layer 90.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },
                    {
                        id: 11,
                        img: 'images_secur/Layer 91.png',
                        title: 'ВИДЕОКАМЕРА HAC-HDW120EMP-A-036B-S3',
                        price: '2.822'
                    },
                    {
                        id: 12,
                        img: 'images_secur/Layer 85.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '8.000'
                    }

                ],
                swiperOption: {
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    },
                    slidesPerView: 3,
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

    .slider_container {
        max-width: 865px;
        min-height: 369px;
        border-radius: 30px;
        background-color: #ffffff;
    }


    .slider-sort {

        display: -webkit-box;

        display: -ms-flexbox;

        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        margin-left: 20px;

    }
    .button-top {
        width: 114px;
        height: 31px;
        border-radius: 16px;
        background-color: #ff5757;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
    }
    .button-top:hover{
        background-color: #ff3131;
    }
    .top {
        color: #ffffff;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 500;
        line-height: 14px;
        text-transform: uppercase;
        letter-spacing: 0.17px;
    }
    .new {
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 500;
        line-height: 14px;
        text-decoration: underline;
        letter-spacing: 0.17px;
        margin-left: 15px;
    }
    .action {
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 500;
        line-height: 14px;
        text-decoration: underline;
        letter-spacing: 0.17px;
        margin-left: 15px;
    }

    .new:hover {
        color: black;
    }
    .action:hover {
        color: black;
    }

    .slider {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-pack: distribute;
        justify-content: space-around;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        margin-top: 30px;
    }
    @media (max-width: 430px) {
        .slider_container {
            display: none;
        }
    }
</style>