<template>
    <div class="title-block">
        <div class="title-block_name">
            <p>Статьи и обзоры</p>
        </div>
        <div class="title-block_container">

            <div class="title-one">
                <img src="images_secur/Layer 55.png" alt="">
                <span class="direction">Монтаж видеодомофона</span>
                <img class="text" src="images_secur/text_1.png" alt="">
            </div>
            <div class="title-two">
                <img src="images_secur/Layer 56.png" alt="">
                <span class="direction">Как выбрать сигнализацыю</span>
                <img class="text" src="images_secur/text_2.png" alt="">
            </div>
            <div class="title-three">
                <img src="images_secur/Layer 42.png" alt="">
                <span class="direction">Правильный выбор eлектрозамка</span>
                <img class="text" src="images_secur/text_3.png" alt="">
            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: "TitlesComponent"
    }
</script>

<style>
    .title-block {
        width: 100%;
        max-width: 865px;
        min-height: 480px;
        border-radius: 30px;
        background-color: #ffffff;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
    }
    .title-block_container {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-pack: distribute;
        justify-content: space-around;
        -ms-flex-line-pack: center;
        align-content: center;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        margin-top: 30px;
    }

    .title-block_name {
        width: 133px;
        height: 12px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 14px;
        font-weight: 700;
        line-height: 20px;
        text-transform: uppercase;
        letter-spacing: -0.35px;
        margin-top: 40px;
        margin-left: 40px;
    }
    .title-one {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        width: 30%;
    }
    .title-two {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        width: 30%;
    }
    .title-three {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        width: 30%;
    }
    .direction {
        max-width: 221px;
        height: 12px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 600;
        line-height: 14px;
        text-decoration: underline;
        text-transform: uppercase;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-pack: start;
        -ms-flex-pack: start;
        justify-content: flex-start;
        margin-top: 20px;
    }
    .text {
        margin-top: 20px;
    }
    @media (max-width: 430px) {
        .title-block_container {
            -webkit-box-orient: vertical;
            -webkit-box-direction: normal;
            -ms-flex-direction: column;
            flex-direction: column;
            -webkit-box-pack: center;
            -ms-flex-pack: center;
            justify-content: center;
            -webkit-box-align: center;
            -ms-flex-align: center;
            -ms-grid-row-align: center;
            align-items: center;
        }
        .title-block_name {
            margin: 20px 140px;
        }
        .title-one{
            width: 60%;
        }
        .title-two {
            width: 60%;
            margin-top: 10px;
        }
        .title-three {
            width: 60%;
            margin-top: 10px;
        }
        .text {
            margin-bottom: 20px;
        }
    }
</style>