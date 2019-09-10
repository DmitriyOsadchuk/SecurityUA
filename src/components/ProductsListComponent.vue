<template>

    <div class="products">
        <div class="product_sort">
            <div class="title_sort">Показать по:</div>
            <ul class="sort_category">
                <li class="category_products"><a href="#">Цене</a></li>
                <li class="category_products"><a href="#">Алфавиту</a></li>
                <li class="category_products"><a href="#">Популярности</a></li>
            </ul>

        </div>
        <div class="products_list">
            <product-card-component v-for="(product, id) in products" :item="product" :key="id"/>
        </div>

    </div>

    
</template>

<script>
    import ProductCardComponent from '@/components/ProductCardComponent'

    export default {
        name: "ProductsListComponent",
        data() {
            return {
                products: [
                    {
                        id: 1,
                        img: 'images_secur/Layer 80.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '2.574'
                    },
                    {
                        id: 2,
                        img: 'images_secur/Layer 81.png',
                        title: 'ВИДЕОКАМЕРА HAC-HDW120EMP-A-036B-S3',
                        price: '2.822'
                    },
                    {
                        id: 3,
                        img: 'images_secur/Layer 82.png',
                        title: 'КОМПЛЕКТ ВИДЕОНАБЛЮДЕНИЯ ATIS STARTER KIT IP 4EXT',
                        price: '8.000'
                    },
                    {
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
                    },

                ]
            }
        },
        components: {
            ProductCardComponent
        }

    }
</script>

<style>
    .products {
        max-width: 865px;
        min-height: 1258px;
        border-radius: 30px;
        background-color: #ffffff;

    }

    .product_sort {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-align: baseline;
        -ms-flex-align: baseline;
        align-items: baseline;



    }
    .title_sort {
        /*width: 72px;*/
        height: 10px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 12px;
        font-weight: 500;
        line-height: 14px;
        letter-spacing: -0.3px;
        margin-left: 20px;
        padding: 30px;


    }
    .sort_category  {
        width: 253px;
        height: 34px;
        border-radius: 17px;
        background-color: #ededee;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-pack: space-evenly;
        -ms-flex-pack: space-evenly;
        justify-content: space-evenly;
        /*flex-wrap: nowrap;*/
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
    }

    .category_products {
        height: 12px;
        color: #8e8d93;
        font-family: "Helvetica Neue";
        font-size: 12px;
        font-weight: 500;
        line-height: 14px;
        letter-spacing: -0.3px;
        border-bottom: 1px dotted grey;
    }

    .category_products:hover{
        color: black;
    }

    .products_list {
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
    }

    @media (max-width: 430px) {
        .title_sort {
            padding: 0;
            margin-right: 5px;
        }
    }

</style>