<template>
    <div class="panel_container">
        <div class="description_panel">
            <div class="title_panel">
                <p>Солнечные пенели</p>
            </div>
            <div class="type_panel">
                <p>поликристаллические</p>
            </div>
            <div class="panel_buy">
                <span class="panel__prise">от 3.990грн</span>
                <button class="product__buy" type="submit">Купить</button>
            </div>

        </div>
    </div>
</template>

<script>

    export default {
        name: "SolarPanelComponent"
    }
</script>

<style>
    .panel_container {
        max-width: 301px;
        height: 369px;
        border-radius: 0 30px 30px 0;
        background-color: #dcdcdc;
        background-image: url('~@/assets/solar_panels.png');

    }
    .description_panel {
        padding: 55px;
    }
    .title_panel {
        width: 152px;
        height: 12px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 13px;
        font-weight: 600;
        line-height: 20px;
        text-transform: uppercase;
        letter-spacing: -0.35px;
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
    .type_panel {
        width: 118px;
        height: 8px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 600;
        line-height: 20px;
        letter-spacing: -0.28px;
    }
    .panel_buy {
        margin-top: 11px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;

    }


    .panel__prise {
        margin: 5px;
        font-size: 20px;
        color: #0060fa;
        font-family: "Helvetica Neue - Condensed Bold";
    }
    .product__buy {
        margin-top: 10px;
    }

</style>