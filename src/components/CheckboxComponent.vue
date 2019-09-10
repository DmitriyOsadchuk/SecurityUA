<template>
    <div class="page_view">
        <div class="look_form">
            <span class="look">Вид</span>
            <button class="form_1"><img class="form_1" src="images_secur/Forma_1.png" alt=""></button>
            <button class="form_2"><img class="form_2" src="images_secur/Forma_2.png" alt=""></button>
        </div>
        <div class="checkbox-block">
            <div class="checkbox-block__container">
                <div v-for="(characteristic, index) in characteristics" :key="index"
                     class="checkbox-block__characteristic-container">
                    <div class="checkbox-block__characteristic">{{characteristic.name}}</div>
                    <div v-for="(option, index) in characteristic.options" :key="index">
                        <input type="checkbox" :id='option+index' name="option">
                        <label :for='option+index'>{{option}}</label>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "CheckboxComponent",
        data() {
            return {
                characteristics: [
                    {
                        name: 'Производитель',
                        options: ['ATIS', 'Dahua', 'Hikvision']
                    },
                    {
                        name: 'Тип установки',
                        options: ['Внутренняя', 'Наружная']
                    },
                    {
                        name: 'Разрешение камеры',
                        options: ['1Mp', '1.3Mp', '1.4Mp', '2Mp', '2.4Mp', '3Mp', '4Mp', '5Mp']
                    },
                    {
                        name: 'Максимальное разрешение записи',
                        options: ['1280x720', '1280x960', '1920x1080', '2048x1536', '2304x1536']
                    }
                ]
            }
        }
    }
</script>

<style>
    .look_form {
        width: 100%;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -ms-flex-wrap: nowrap;
        flex-wrap: nowrap;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        margin-top: 40px;
    }
    .look {
        width: 24px;
        height: 11px;
        color: #66666a;
        font-family: "Helvetica Neue";
        font-size: 12px;
        font-weight: 500;
        line-height: 14px;
        letter-spacing: -0.3px;
        margin-left: 120px;
        margin-bottom: 8px;
    }
    .form_1 {
        margin-left: 10px;
    }
    .form_2 {
        margin-left: 5px;
    }
    .checkbox-block {
        max-width: 257px;
        background-color: #c2c2c2;
        border-radius: 25px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        text-align: left;
        color: #66666a;
        font-size: 14px;
        font-weight: 400;
        line-height: 30px;
        letter-spacing: -0.35px;
        margin-top: 35px;
    }

    .checkbox-block__container {
        margin: auto 30px;
    }

    .checkbox-block__characteristic-container {
        margin: 30px auto;

    }

    .checkbox-block__characteristic {
        margin: 10px auto;
        font-size: 16px;
        font-weight: 500;
        line-height: 14px;
        letter-spacing: -0.4px;
    }
    @media (max-width: 1024px){
        .page_view {
            display: none;
        }
    }
</style>