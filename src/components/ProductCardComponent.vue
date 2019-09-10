<template>
    <div class="product">
        <div class="product__image-container">
            <img class="product__image" :src="`${item.img}`" alt="">
        </div>
        <div class="product__title">{{item.title}}</div>
        <div class="product__price">{{item.price}} <span class="product__uah">грн</span>
            <button class="product__buy" type="submit">Купить</button>
        </div>
    </div>

</template>

<script>
    export default {
        name: "ProductCardComponent",
        data() {
            return {}
        },
        props: {
            item: {
                type: Object,
                required: true
            }
        },
    }
</script>

<style>
    .product {
        width: 260px;
        height: 260px;

        margin: 10px 10px 15px 10px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        position: relative;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-around;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        text-align: center;
        margin-right: 18px;

    }

    .product__image-container {
        position: relative;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
    }

    .product__image {
        width: 170px;
        height: 170px;

    }

    .product__title {
        width: 187px;
        height: 24px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 500;
        line-height: 14px;
        text-transform: uppercase;
    }
    .product__title:hover {
        /*color: #ff373b;*/
        color: black;
    }

    .product__price {
        margin: 5px;
        font-size: 20px;
        color: #0060fa;
        font-family: "Helvetica Neue - Condensed Bold";
    }

    .product__uah {
        font-family: "Myriad Pro";
        font-weight: 400;
        letter-spacing: -0.49px;
    }

    .product__buy {
        width: 80px;
        height: 28px;
        border-radius: 14px;
        font-family: "Helvetica Neue";
        color: #ffffff;
        background-color: #0060fa;
    }
    .product__buy:hover {
        background-color: #003ffa;
    }

    .product__price .product__buy {
        margin-left: 15px;
    }

</style>