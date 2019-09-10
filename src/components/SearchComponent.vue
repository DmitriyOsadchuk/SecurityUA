<template>
    <div class="search_container">
        <div class="logo">
            <div class="">
                <img src="images_secur/logo.png">
            </div>

        </div>
        <div class="search_contacts">
            <div class="search_call">
                <span class="phone-code">+38096</span> <span class="phone">00 00 00</span>
            </div>
            <div class="sep">|</div>

            <div class="search_call">
                <span class="phone-code">+38096</span> <span class="phone">00 00 00</span>
            </div>
            <div class="sep">|</div>
            <div class="search_call">
                <div class="adress-row">
                    <span class="adress">Киев, ул. Матроса Кошки 7,<p>офис 620</p></span>
                </div>
            </div>
        </div>


        <div class="search" id="findBox">
            <form>
                <input class="text_input" type="text" placeholder="Найти на сайте..." autocomplete="off">
                <button type="submit">
                    <i class="fa fa-search"></i>
                </button>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SearchComponent"
    }
</script>

<style>
    .search_container {
        max-width: 1550px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        margin: auto;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-line-pack: center;
        align-content: center;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: wrap;
        flex-wrap: nowrap;
        padding-left: 22px;
        padding-right: 50px;
    }
    .logo {
        margin-bottom: 9px;
    }
    .search_contacts {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-pack: space-evenly;
        -ms-flex-pack: space-evenly;
        justify-content: space-evenly;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        width: 865px;
    }
    .search_call {
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

    }
    * {box-sizing: border-box;}
    form {
        position: relative;
        width: 300px;
        margin: 0 auto;
    }
    input::-webkit-input-placeholder {
        color: #dddce2;
    }
    input::-moz-placeholder {
        color: #dddce2;
    }
    input:-ms-input-placeholder {
        color: #dddce2;
    }
    input::placeholder {
        color: #dddce2;
    }
    .search {
        background: #8e8d93;
        border-radius: 5px;
        border: 1px solid #8e8d93;
    }
    .search input {
        width: 100%;
        height: 42px;
        padding-left: 10px;
        border: 0px solid #8e8d93;
        border-radius: 5px;
        outline: none;
        background: #8e8d93;
        color: #e7efff;
    }
    .search button {
        position: absolute;
        top: 0;
        right: 0px;
        width: 42px;
        height: 42px;
        border: none;
        background: #dddce2;
        border-radius: 0 5px 5px 0;
        cursor: pointer;
    }
    .search button i {
        font-size: 20px;
        color: #8e8d93;
    }

    @media (min-width: 1200px) {
        .search_contacts {
            margin: 10px 100px;
        }
    }
    @media (max-width: 1199px) {
        .search_contacts {
            display: none;
        }
    }
    @media (max-width: 430px) {
        .search {
            display: none;
        }
    }
</style>