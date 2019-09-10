<template>
    <div class="main-slider">
        <div class="main-slider_info">
            <div class="slider_info_title">
                <div class="slider_info_title1">{{slides[currentIndex].title1}}</div>
                <div class="slider_info_title2">{{slides[currentIndex].title2}}</div>
            </div>
            <div class="slider_info_description">{{slides[currentIndex].description}}</div>
            <div class="indicators">
                <div v-for="(indicator, index) in slides" :key="index">
                    <div>{{indicator.id}}</div>
                    <button @click="currentIndex = index"
                            :class="['indicator', {active: currentIndex===index}]">
                    </button>
                </div>
            </div>
        </div>
        <div class="camera_img_container">
            <img src="/images_secur/main_camera_1.png" class="camera-img"/>
        </div>

        <div class="main_slider_logo">
            <div class="slider_logo" v-for="(logotype, index) in logotypes" :key="index">
                <div><img :src="`${logotype}`"/></div>
            </div>
        </div>
        <div class="modal-block">
            <div class="play_icon">
                <button type="button" class="btn" @click="showModal">
                    <img src="images_secur/play.png" class="play">
                </button>
            </div>
            <modal-component v-show="isModalVisible" @close="closeModal"/>

        </div>


    </div>
</template>

<script>
    import ModalComponent from '@/components/ModalComponent.vue'
    export default {
        name: "MainSliderComponent",

        data() {
            return {
                currentIndex: 0,
                timer: null,
                isModalVisible: false,
                slides: [
                    {
                        id: '01',
                        title1: 'Искусство',
                        title2: 'Безопасности',
                        description: 'В камерах HIKVISION встроены современные технологи подавления шумов, так что ваша изображение будет всегда оставаться чистым.'
                    },
                    {
                        id: '02',
                        title1: 'Принцип',
                        title2: 'Надежности',
                        description: 'Lorem Ipsum - это текст-"рыба", часто используемый в печати и вэб-дизайне. Lorem Ipsum является стандартной "рыбой" для текстов на латинице с начала XVI века.'
                    },
                    {
                        id: '03',
                        title1: 'Гарантия',
                        title2: 'Качества',
                        description: 'Есть много вариантов Lorem Ipsum, но большинство из них имеет не всегда приемлемые модификации, например, юмористические вставки или слова, которые даже отдалённо не напоминают латынь.'
                    }

                ],
                logotypes: [
                    'images_secur/commax_logo.png',
                    'images_secur/ajhua_logo.png',
                    'images_secur/ifsec_logo.png',
                    'images_secur/hikvision_logo.png',
                    'images_secur/yli electronic_logo.png',
                    'images_secur/Garret_logo.png',
                ],
            }
        },
        components: {
            ModalComponent
        },
        mounted: function () {
            this.startRotation();
            this.logoRotation();
        },
        methods: {
            startRotation: function () {
                this.timer = setInterval(this.next, 3000);
            },
            next: function () {
                if (this.currentIndex === this.slides.length - 1) {
                    this.currentIndex = -1
                }
                this.currentIndex += 1
            },
            logoRotation: function () {
                this.play = setInterval(this.move, 1000);
            },
            move: function () {
                this.logotypes = this.logotypes.concat(this.logotypes.splice(0, 1));
            },
            showModal() {
                this.isModalVisible = true;
            },
            closeModal() {
                this.isModalVisible = false;
            }

        }
    }
</script>

<style scoped>
    .main-slider {
        background-color: white;
        border-radius: 30px;
        background-image: url("/images_secur/Layer 23.png");
        background-position: bottom 1px right 0px;
        max-width: 865px;
        min-height: 545px;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
    }

    @media screen and (max-width: 865px) {
        .main-slider {
            display: none;
        }
    }

    .main-slider_info {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
        -ms-flex-pack: distribute;
        justify-content: space-around;
        color: #ffffff;
        margin: 35px 0 108px 45px;
    }

    .slider_info_title {
        font-size: 75px;
        font-weight: 100;
        letter-spacing: -0.27px;
    }

    .slider_info_title1 {
        text-align: start;
    }

    .slider_info_title2 {
        text-align: end;
    }

    .slider_info_description {
        text-align: start;
        width: 460px;
        font-size: 14px;

    }

    .indicators {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        text-align: left;
        font-size: 11px;
        margin: 10px;
    }

    .indicator {
        width: 55px;
        height: 4px;
        border-radius: 2px;
        background-color: #ffffff;
        border: none;
        outline: none !important;
        cursor: pointer;
        margin-right: 13px;
    }

    .indicator.active {
        width: 133px;
    }
    .camera_img_container {
        position: absolute;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-line-pack: center;
        align-content: center;
        margin-left: 615px;

    }
    .camera-img {
        -ms-flex-item-align: center;
        align-self: center;
        margin-top: 58px;
    }
    .main_slider_logo {
        position: absolute;
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
        width: 705px;
        margin-top: 445px;
        margin-left: 13px;
    }

    .slider_logo {
        margin: 10px;
    }
    .play_icon {
        position: absolute;
        margin-top: 440px;
        margin-rightt: 260px;
    }
    .play {
        position: absolute;
        right: 62px;
    }
    .play:hover {
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }
    @media(min-width: 1920px) {
        .camera_img_container{
            margin-left: 625px;
        }
    }

</style>