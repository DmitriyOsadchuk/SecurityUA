<template>
    <div id="app">
        <header-component/>
        <search-component/>
        <div class="container">
            <div class="row-container">
                <div class="col_rigth">
                    <filter-component/>
                </div>
                <div class="col_center">
                    <main-slider-component/>
                </div>
                <div class="col_left">
                    <basket-component/>
                </div>
            </div>

            <div class="row-container">
                <div class="col_rigth">
                    <solar-panel-component/>
                </div>
                <div class="col_center">
                    <slider-component/>
                </div>
                <div class="col_left">
                    <small-slider-component/>
                </div>
            </div>

            <div class="row-container">
                <div class="col_rigth">

                </div>
                <div class="col_center">
                    <products-list-component/>
                    <request-items-component/>
                    <titles-component/>
                </div>
                <div class="col_left">
                    <checkbox-component/>
                </div>
            </div>
        </div>
        <footer-component/>
    </div>
</template>
<script>
    import HeaderComponent from './components/HeaderComponent'
    import SliderComponent from './components/SliderComponent'
    import FooterComponent from './components/FooterComponent'
    import SearchComponent from './components/SearchComponent'
    import FilterComponent from './components/FilterComponent'
    import ProductsListComponent from './components/ProductsListComponent'
    import MainSliderComponent from './components/MainSliderComponent'
    import RequestItemsComponent from './components/RequestItemsComponent'
    import CheckboxComponent from './components/CheckboxComponent'
    import TitlesComponent from './components/TitlesComponent'
    import SmallSliderComponent from './components/SmallSliderComponent'
    import SolarPanelComponent from './components/SolarPanelComponent'
    import BasketComponent from './components/BasketComponent'
    export default {
        components: {
            HeaderComponent,
            SliderComponent,
            FooterComponent,
            SearchComponent,
            FilterComponent,
            ProductsListComponent,
            MainSliderComponent,
            RequestItemsComponent,
            CheckboxComponent,
            TitlesComponent,
            SmallSliderComponent,
            SolarPanelComponent,
            BasketComponent,

        }
    }
</script>


<style>
    * {
        margin: 0;
        padding: 0;

    }

    body {
        font-family: Segoe UI, Frutiger, Frutiger Linotype, Dejavu Sans, Helvetica Neue, Arial, Font Awesome, sans-serif;
        font-size: 12px;
        background-image: url('~@/assets/background_image.png'), linear-gradient(#ffffff, gainsboro);
        background-repeat: no-repeat;
        background-position: center bottom;
        background-size: 100% ;
        margin: 0;
    }
    a {
        text-decoration: none;
        color: inherit;
    }

    li {
        list-style: none;
    }

    button {
        border: none;
        outline: none!important;
        cursor: pointer;
        background-color: transparent;
    }

    .container {
        max-width: 1550px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        margin: auto;
        margin-top: 40px;

    }
    main {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
    }
    .row-container {
        width: 100%;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-flow: row wrap;
        flex-flow: row wrap;
    }

    .col_rigth {
        width: 16%;
        max-width: 301px;
    }
    .col_center {
        width: 62%;
        max-width: 865px;
    }
    .col_left {
        width: 22%;
        max-width: 280px;
        margin-left: 3px;
    }
    @media (min-width: 576px) {
        main {
            -webkit-box-orient: horizontal;
            -webkit-box-direction: normal;
            -ms-flex-direction: column;
            flex-direction: row;
        }
    }
    @media (max-width: 1024px) {
        .col_center {
            width: 100%;
            margin: auto;
        }
        .col_rigth {
            display: none;
        }
        .col_left {
            display: none;
        }
    }
</style>
