<template>
    <div class="basket_container_block">
        <div class="basket_container">
            <div class="basket_item">
                <div class="basket-icon">
                    <img src="images_secur/basket.png" class="basket_logo">
                </div>
                <div class="basket-title-col">
                    <div class="basket-title-name">
                        <span class="basket-title">Корзина</span>
                    </div>
                    <div class="basket-prise">
                        <span class="value">2.540грн</span>
                    </div>
                </div>

            </div>
            <div class="basket_category">
                <div class="category">
                    <div class="video_cams_title">
                        <p>Видео-камери</p>
                    </div>
                    <div class="video_cams_icon">
                        <img src="images_secur/video_cams.png" alt="">
                    </div>

                </div>
                <div class="category">
                    <div class="video_recoders_title">
                        <p>Видео-регистраторы</p>
                    </div>
                    <div class="video_recoders_icon">
                        <img src="images_secur/video_recorders.png" alt="">
                    </div>
                </div>
                <div class="category">
                    <div class="alarm_systems_title">
                        <p>Cигнализации</p>
                    </div>
                    <div class="alarm_systems_icon">
                        <img src="images_secur/alarm_system.png" alt="">
                    </div>
                </div>
                <div class="category">
                    <div class="call_panels_title">
                        <p>Вызывные панели</p>
                    </div>
                    <div class="call_panels_icon">
                        <img src="images_secur/call_panels.png" alt="">
                    </div>
                </div>
                <div class="category">
                    <div class="intercoms_title">
                        <p>Домофоны</p>
                    </div>
                    <div class="intercoms_icon">
                        <img src="images_secur/intercoms.png" alt="">
                    </div>
                </div>
            </div>
         </div>
    </div>
</template>

<script>
    export default {
        name: "BasketComponent"
    }
</script>

<style>
    .basket_container_block {
        max-width: 290px;
    }
    .basket_container {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -webkit-box-pack: start;
        -ms-flex-pack: start;
        justify-content: flex-start;
        margin-left: 80px;

    }
    .basket_item {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;

    }

    .basket-title-col {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        margin-left: 10px;
    }
    .basket-title {
        width: 57px;
        height: 14px;
        color: #ff5757;
        font-family: "Helvetica Neue";
        font-size: 14px;
        font-weight: 500;
        line-height: 28px;
        letter-spacing: -0.35px;
        margin-left: 5px;
    }
    .value {
        width: 84px;
        height: 28px;
        border-radius: 14px;
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
        color: white;
    }
    .basket_category {
        margin-top: 30px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 12px;
        font-weight: 500;
        line-height: 14px;
        letter-spacing: -0.3px;
    }

    .category {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-line-pack: center;
        align-content: center;
        margin: 18px;
        padding: 3px
    }
    .video_cams_icon:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }
    .video_recoders_icon:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }
    .alarm_systems_icon:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }
    .call_panels_icon:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }
    .intercoms_icon:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }

    .video_cams_title:hover {
        color: black;
        width: 43px;
        height: 26px;

    }
    .video_recoders_title:hover {
        color: black;
        width: 79px;
        height: 26px;
    }
    .alarm_systems_title:hover {
        color: black;
        width: 82px;
        height: 12px;
    }
    .call_panels_title {
        width: 62px;
        height: 24px;
    }
    .call_panels_title:hover {
        color: black;
    }
    .intercoms_title:hover {
        color: black;
        width: 67px;
        height: 12px;
    }
    .video_cams_icon {
        margin-left: 20px;
    }
</style>