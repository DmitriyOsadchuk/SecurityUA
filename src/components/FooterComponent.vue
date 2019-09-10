<template>
    <footer>
        <div class="footer-brand">

            <div class="footer-brand_logo">
                <img class="logo" src="images_secur/logo.png">
            </div>
            <div class="text_logo">
                <img src="images_secur/Slice_1.png">
            </div>

        </div>


        <div class="footer-contacts">
            <div class="footer_call">
                <span class="phone-code">+38096</span> <span class="phone">00 00 00</span>
                <div class="phone_icon">
                    <img src="images_secur/phone_call.png" class="image_phone">
                </div>
            </div>
            <div class="sep">|</div>

            <div class="footer_call">
                <span class="phone-code">+38096</span> <span class="phone">00 00 00</span>
                <div class="mobile_icon">
                    <img src="images_secur/mobile_call.png" class="image_mobile">
                </div>
            </div>
            <div class="sep">|</div>
            <div class="footer_call">
                <div class="adress-row">
                    <span class="adress">Киев, ул. Матроса Кошки 7,<p>офис 620</p></span>
                </div>
            </div>
        </div>


        <div class="footer_social">
            <div class="footer_call">
                <li class="footer_social_network">
                    <a href="https://www.youtube.com"><img src="images_secur/Layer_59.png" class="you-tube"></a>
                    <span class="our_channel">Наш канал <p>на YouTube</p></span>
                    <div class="sep">|</div>
                    <a href="https://www.facebook.com"> <img src="images_secur/facebook.png" class="facebook"></a>
                </li>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "FooterComponent"
    }
</script>

<style>
    footer {
        margin: auto;
        max-width: 1550px;
        width: 100%;
        min-height: 120px;
        background-color: #8e8d93;
        color: #ffffff;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-align: stretch;
        -ms-flex-align: stretch;
        -ms-grid-row-align: stretch;
        align-items: stretch;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
    }

    footer > div {
        -webkit-box-flex: 1;
        -ms-flex-positive: 1;
        flex-grow: 1;
        border-radius: 0;
    }

    .footer-brand {
        width: 16%;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-line-pack: center;
        align-content: center;
        -webkit-box-ordinal-group: 2;
        -ms-flex-order: 1;
        order: 1;
        -ms-flex-direction: column;
        flex-direction: column;
    }

    .logo {
        width: 127px;
        height: 35px;
    }

    .text_logo {
        margin-left: 10px;
    }

    .footer-contacts {
        width: 61%;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-ordinal-group: 4;
        -ms-flex-order: 3;
        order: 3;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        -webkit-box-pack: space-evenly;
        -ms-flex-pack: space-evenly;
        justify-content: space-evenly;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        margin: 0 1px;
    }

    .footer_call {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -ms-grid-column-align: baseline;
        justify-items: baseline;
        margin: 10px;
    }

    .phone {
        font-family: "Helvetica Neue - Condensed Bold";
        font-size: 32px;
        font-weight: 400;
        letter-spacing: -0.7px;
        margin-left: 5px;

    }

    .phone-code {
        width: 48px;
        height: 11px;
        font-family: Helvetica;
        font-size: 14px;
        font-weight: 400;
        line-height: 26px;
        margin-top: 3px;
    }

    .image_phone {
        width: 23px;
        height: 23px;
        margin-top: 8px;
        margin-left: 13px;
    }

    .image_mobile {
        width: 15px;
        height: 26px;
        margin-top: 8px;
        margin-left: 13px;
    }

    .sep {
        display: none;
        width: 1px;
        height: 23px;
        opacity: 0.5;
        -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=50)";
    }

    .footer_social {
        width: 22%;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -ms-grid-column-align: center;
        justify-items: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-line-pack: center;
        align-content: center;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-ordinal-group: 3;
        -ms-flex-order: 2;
        order: 2;
    }

    .footer_social_network {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -ms-flex-line-pack: center;
        align-content: center;
        margin-right: 50px;
    }

    .facebook {
        margin: 20px;
    }

    .facebook:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
        opacity: 0.8;
        -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=80)";
    }

    .you-tube:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
        opacity: 0.8;
        -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=80)";
    }

    .our_channel {
        width: 56px;
        height: 21px;
        font-family: "Helvetica Neue";
        font-size: 11px;
        font-weight: 400;
        line-height: 12px;
        margin: 15px;
    }

    @media (min-width: 1200px) {
        footer {
            background-color: transparent;
        }

        footer > div {
            background-color: #8e8d93;
        }

        .footer-brand {
            border-radius: 0 30px 0 0;
        }

        .footer-contacts {
            border-radius: 30px 30px 0 0;
        }

        .footer_social {
            border-radius: 30px 0 0 0;
        }

        .footer-contacts {
            -webkit-box-ordinal-group: 3;
            -ms-flex-order: 2;
            order: 2;
        }

        .sep {
            display: inline;
        }
    }
    @media (max-width: 769px) {
        .footer_social_network {
            margin-left: 50px;
            margin-right: 0;
        }
    }
    @media (max-width: 426px) {
        .footer-brand {
            margin: 5px 10px 0 15px;

            width: 100%;
        }
        .footer-contacts {
            width: 100%;
        }
        .footer_social_network{
            width: 100%;
            margin-right: 0;
        }

    }
</style>