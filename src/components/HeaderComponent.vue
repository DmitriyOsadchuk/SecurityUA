<template>
    <header>
        <div class="header-container">
            <span class="header_lang">
                <a rel="nofollow"  class="header_nav-item" href="#">MD</a>
                <a rel="nofollow"  class="header_nav-item" href="#">RU</a>
                <a rel="nofollow"  class="header_nav-item" href="#">EN</a>
            </span>
            <span class="header_nav">
                <a rel="nofollow"  class="header_nav-item" href="#">Акции</a>
                <a rel="nofollow"  class="header_nav-item" href="#">Статьи</a>
                <a rel="nofollow"  class="header_nav-item" href="#">Услуги</a>
                <a rel="nofollow"  class="header_nav-item" href="#">Сервисный центр</a>
                <a rel="nofollow"  class="header_nav-item" href="#">Сотруднечество</a>
                <a rel="nofollow"  class="header_nav-item" href="#">Контакти</a>
            </span>

            <div class="gamburger_container">
                <input id="toggle" type="checkbox">
                <label class="toggle-container" for="toggle">
                    <span class="button button-toggle"></span>
                </label>
                <nav class="nav">
                    <a rel="nofollow"  class="nav-item" href="#">Акции</a>
                    <a rel="nofollow"  class="nav-item" href="#">Статьи</a>
                    <a rel="nofollow"  class="nav-item" href="#">Услуги</a>
                    <a rel="nofollow"  class="nav-item" href="#">Сервисный центр</a>
                    <a rel="nofollow"  class="nav-item" href="#">Сотруднечество</a>
                    <a rel="nofollow"  class="nav-item" href="#">Контакти</a>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: "HeaderComponent"
    }
</script>

<style>
    header {
        margin: 20px 55px;
    }

    .header-container {
        max-width: 1550px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        margin: auto;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-line-pack: center;
        align-content: center;
        color: #8e8d93;
        font-family: "Helvetica Neue";
        font-size: 12px;
        font-weight: 400;
        line-height: 14.4px;
    }

    .header_lang {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        color: #8e8d93;
        font-family: "Helvetica Neue";
        font-weight: 300;
        font-size: 12px;
        margin: 10px;
    }

    .header_nav {
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
        color: #8e8d93;
        font-family: "Helvetica Neue";
        font-weight: 300;
        font-size: 12px;
    }

    .header_nav-item {
        margin: 10px;
    }

    .header_nav-item:hover {
        color: black;
    }
    .gamburger_container {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: start;
        -ms-flex-pack: start;
        justify-content: flex-start;

    }
    #toggle {
        position: absolute;
        left: -100%;
        top: -100%;
    }

    #toggle:checked ~ .toggle-container .button-toggle:before {
        -webkit-transform: translateY(-50%) rotate(45deg) scale(1);
        transform: translateY(-50%) rotate(45deg) scale(1);
    }
    #toggle:checked ~ .toggle-container .button-toggle:after {
        -webkit-transform: translateY(-50%) rotate(-45deg) scale(1);
        transform: translateY(-50%) rotate(-45deg) scale(1);
    }
    #toggle:checked ~ .nav {
        pointer-events: auto;
        -webkit-transform: translate(20px, 20px);
        transform: translate(20px, 20px);
    }
    #toggle:checked ~ .nav .nav-item {
        color: #8e8d93;
        letter-spacing: 0;
        font-family: "Helvetica Neue";
        font-weight: 300;
        font-size: 12px;
        height: 40px;
        line-height: 40px;
        margin-top: 0;
        opacity: 1;
        -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=100)";
        -webkit-transform: scaleY(1);
        transform: scaleY(1);
        -webkit-transition: 0.5s, opacity 0.1s;
        transition: 0.5s, opacity 0.1s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(1) {
        -webkit-transition-delay: 0.15s;
        transition-delay: 0.15s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(1):before {
        -webkit-transition-delay: 0.15s;
        transition-delay: 0.15s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(2) {
        -webkit-transition-delay: 0.1s;
        transition-delay: 0.1s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(2):before {
        -webkit-transition-delay: 0.1s;
        transition-delay: 0.1s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(3) {
        -webkit-transition-delay: 0.05s;
        transition-delay: 0.05s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(3):before {
        -webkit-transition-delay: 0.05s;
        transition-delay: 0.05s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(4) {
        -webkit-transition-delay: 0s;
        transition-delay: 0s;
    }
    #toggle:checked ~ .nav .nav-item:nth-child(4):before {
        -webkit-transition-delay: 0s;
        transition-delay: 0s;
    }
    #toggle:checked ~ .nav .nav-item:before {
        opacity: 0;
        -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";
    }

    .button-toggle {
        position: absolute;
        display: inline-block;
        width: 20px;
        height: 20px;
        margin: 25px;
        background-color: transparent;
        border: none;
        cursor: pointer;
        border-radius: 100%;
        -webkit-transition: 0.6s;
        transition: 0.6s;
    }
    .button-toggle:hover {
        box-shadow: 0 0 0 8px rgba(0, 0, 0, 0.1), inset 0 0 0 20px rgba(0, 0, 0, 0.1);
    }
    .button-toggle:before, .button-toggle:after {
        position: absolute;
        content: '';
        top: 50%;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: #EC7263;
        border-radius: 5px;
        -webkit-transition: 0.5s;
        transition: 0.5s;
    }
    .button-toggle:before {
        -webkit-transform: translateY(-50%) rotate(45deg) scale(0);
        transform: translateY(-50%) rotate(45deg) scale(0);
    }
    .button-toggle:after {
        -webkit-transform: translateY(-50%) rotate(-45deg) scale(0);
        transform: translateY(-50%) rotate(-45deg) scale(0);
    }

    .nav {
        display: inline-block;
        margin: 25px 25px 20px;
        pointer-events: none;
        -webkit-transition: 0.5s;
        transition: 0.5s;
    }

    .nav-item {
        position: relative;
        display: inline-block;
        float: left;
        clear: both;
        color: transparent;
        font-size: 14px;
        letter-spacing: -6.2px;
        height: 7px;
        line-height: 7px;
        text-transform: uppercase;
        white-space: nowrap;
        -webkit-transform: scaleY(0.2);
        transform: scaleY(0.2);
        -webkit-transition: 0.5s, opacity 1s;
        transition: 0.5s, opacity 1s;
    }
    .nav-item:nth-child(1) {
        -webkit-transition-delay: 0s;
        transition-delay: 0s;
    }
    .nav-item:nth-child(1):before {
        -webkit-transition-delay: 0s;
        transition-delay: 0s;
    }
    .nav-item:nth-child(2) {
        -webkit-transition-delay: 0.05s;
        transition-delay: 0.05s;
    }
    .nav-item:nth-child(2):before {
        -webkit-transition-delay: 0.05s;
        transition-delay: 0.05s;
    }
    .nav-item:nth-child(3) {
        -webkit-transition-delay: 0.1s;
        transition-delay: 0.1s;
    }
    .nav-item:nth-child(3):before {
        -webkit-transition-delay: 0.1s;
        transition-delay: 0.1s;
    }
    .nav-item:nth-child(4) {
        -webkit-transition-delay: 0.15s;
        transition-delay: 0.15s;
    }
    .nav-item:nth-child(4):before {
        -webkit-transition-delay: 0.15s;
        transition-delay: 0.15s;
    }
    .nav-item:nth-child(1) {
        letter-spacing: -8px;
    }
    .nav-item:nth-child(2) {
        letter-spacing: -7px;
    }
    .nav-item:nth-child(n + 4) {
        letter-spacing: -8px;
        margin-top: -7px;
        opacity: 0;
        -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";
    }
    .nav-item:before {
        position: absolute;
        content: '';
        top: 50%;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: #EC7263;
        -webkit-transform: translateY(-50%) scaleY(5);
        transform: translateY(-50%) scaleY(5);
        -webkit-transition: 0.5s;
        transition: 0.5s;
    }

    @media (min-width: 1200px) {
        .header_lang {
            margin: 10px 200px;
        }
    }

    @media (min-width: 992px) {
        .header_lang {
            margin: 10px 100px;
        }
    }

    @media (min-width: 768px) {
        .header_nav {
            -webkit-box-pack: end;
            -ms-flex-pack: end;
            justify-content: flex-end;
        }
    }

    @media (min-width: 1550px) {
        .header-container {
            padding-right: 40px;
        }
    }

    @media (min-width: 576px) {
        .header-container {
            -webkit-box-orient: horizontal;
            -webkit-box-direction: normal;
            -ms-flex-direction: row;
            flex-direction: row;
        }
        .header_nav {
            -ms-flex-flow: row wrap;
            flex-flow: row wrap;
        }
        .gamburger_container {
            display: none;
        }
    }
    @media (max-width: 576px) {
        header {
            margin: 5px 10px;
        }
        .header_lang {
            display: none;
        }
        .header_nav {
            display: none;
        }
    }

</style>