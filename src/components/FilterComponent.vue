<template>
    <aside>
        <div v-for="(category, id) in categories" :key="id" class="filter_category-block">

            <button @click="toggle(category)" :class="['filter__category', {openable : category.subcategories}]">
                <div v-if="category" class="filter_category-toggle"> {{ category.show ? '–' : '+' }}</div>
                <span class="filter_category-name" :class="{ active: category.show }">{{category.name}}</span>

            </button>
        </div>
        <div class="contats-block">
            <div class="adress-row">
                <span class="adress">Киев, ул. Матроса Кошки 7,<p>офис 620</p></span>
            </div>
            <div class="number_phone-row">
                <span class="number_phone">тел./факс: +38906 000 00 00 <p>моб.: +38906 000 00 00</p></span>
            </div>
            <div class="e-mail_adress-row">
                <span class="e-mail_adress">e-mail:<li class="e-mail">mail@gmail.com</li></span>
            </div>
        </div>
    </aside>
</template>

<script>
    export default {
        name: "FilterComponent",
        data() {
            return {
                close: false,
                categories: [
                    {
                        id: 1,
                        name: 'Видеонаблюдение',
                        show: false,

                    },
                    {
                        id: 2,
                        name: 'Домофони',
                        show: false,

                    },
                    {
                        id: 3,
                        name: 'Контроль доступа',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Охранная синализация',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Пожаная синализация',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Блоки питания',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Металодетекторы',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Кабель',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Разное',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Умный дом',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Солничная енергетика',
                        show: false,

                    },
                    {
                        id: 4,
                        name: 'Распродажа',
                        show: false,

                    },


                ],


            }
        },
        methods: {
            toggle(category) {
                category.show = !category.show

            },
        }
    }
</script>

<style>

    .filter__category {
        height: 25px;
        width: 100%;
        font-size: 11px;
        font-weight: 500;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        color: #333333;
        cursor: pointer;
        padding-left: 25px;
    }

    .filter__category:hover {
        color: #ff3131;
    }

    .filter_category-name {
        margin-left: 10px;

        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 700;
        line-height: 28px;
        text-transform: uppercase;
        letter-spacing: -0.28px;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
    }

    .filter_category-name.active {
        color: #ff5757;
    }

    .filter_category-toggle {
        margin: 8px;
        font-size: 25px;
        color: #333333;

    }

    .contats-block {
        height: 100px;
        font-family: Helvetica;
        font-size: 11px;
        font-weight: 400;
        line-height: 14px;
        letter-spacing: 0.17px;
        margin-left: 0px;
        text-align: start;
        margin-top: 35px;
        padding-left: 30px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
    }
    .e-mail_adress {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
    }
    .e-mail {
        color: #ff5757;
        letter-spacing: 0.17px;
        text-decoration: underline;
    }
    .e-mail:hover {
        color: #ff0300;
    }
    @media (max-width: 1024px){
        .filter_category-block{
            display: none;
        }
    }

</style>