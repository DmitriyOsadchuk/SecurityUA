<template>
    <div class="request_container">
        <div class="massage_1">
            <p>Доверьте нам свою безопасность.</p>
        </div>
        <div class="massage_2">
            <p>Оставте заявку сейчас!</p>
        </div>

        <div class="leave_request">
            <button class="leave_massage" type="button">Оставить заявку</button>

            <li class="number"><span class="massage_3">или позвоните нам:</span> +000 00-00-00</li>

        </div>

    </div>
</template>

<script>
    export default {
        name: "RequestItemsComponent"
    }
</script>

<style>
    .request_container {
        max-width: 865px;
        min-height: 296px;
        border-radius: 30px;
        background-image: url('~@/assets/Layer 54.png');
        margin-top: 182px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
    }
    .massage_1 {
        color: #ffffff;
        font-family: "Helvetica Neue - Thin";
        font-size: 20px;
        font-weight: 400;
        line-height: 20px;
        letter-spacing: -0.5px;
        margin-left: 88px;
        margin-top: 70px;
    }
    .massage_2 {
        color: #ffffff;
        font-family: "Helvetica Neue";
        font-size: 36px;
        font-weight: 500;
        line-height: 20px;
        letter-spacing: -0.9px;
        margin-left: 86px;
        margin-top: 13px;
    }
    .leave_request {
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
        -webkit-box-pack: space-evenly;
        -ms-flex-pack: space-evenly;
        justify-content: space-evenly;
        margin-top: 50px;
        margin-right: 60px;
    }

    .leave_massage {
        width: 239px;
        height: 49px;
        border-radius: 25px;
        background-color: #ff5757;
        color: #ffffff;
        font-family: "Helvetica Neue - Thin";
        font-size: 20px;
        font-weight: 400;
        line-height: 20px;
        letter-spacing: 0.5px;
    }
    .leave_massage:hover {
        background-color: #ff3131;
    }
    .number {
        color: #ffffff;
        font-family: "Helvetica Neue - Condensed Bold";
        font-weight: 700;
        letter-spacing: 0.5px;
        font-size: 20px;
        line-height: 20px;
    }
    .massage_3 {
        color: #ffffff;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-weight: 400;
        line-height: 20px;
        letter-spacing: 0.5px;
    }

    @media (max-width: 430px) {
        .request__container {
            margin-top: 0;
        }
        .leave_request {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-orient: vertical;
            -webkit-box-direction: normal;
            -ms-flex-direction: column;
            flex-direction: column;
            -webkit-box-pack: center;
            -ms-flex-pack: center;
            justify-content: center;
            -ms-flex-line-pack: center;
            align-content: center;
            -webkit-box-align: center;
            -ms-flex-align: center;
            align-items: center;
            margin: 40px 50px;
        }
        .massage_1 {
            margin: 33px 70px;
        }
        .massage_2 {
            margin: 10px 45px;
        }
        .massage_3 {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-orient: vertical;
            -webkit-box-direction: normal;
            -ms-flex-direction: column;
            flex-direction: column;
        }
    }
    @media (max-width: 376px) {
        .leave_request {
            margin: 20px 50px;
        }
    }
</style>