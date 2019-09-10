<template>
    <transition name="modal-fade">
        <div class="modal-backdrop">
            <div class="modal">
                <iframe width="720" height="480" src="https://www.youtube.com/embed/goSQhAwrjzM" frameborder="0" allowfullscreen></iframe>
                <button type="button" class="btn-close" @click="close" aria-label="Close modal">Close video</button>
            </div>
        </div>
    </transition>
</template>

<script>
    export default {
        name: "ModalComponent",
        methods: {
            close() {
                this.$emit('close');
            },
        }
    }
</script>

<style>
    .modal-backdrop {
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        background-color: rgba(0, 0, 0, 0.8);
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
    }

    .modal {
        background: #FFFFFF;
        box-shadow: 2px 2px 20px 1px;
        overflow-x: auto;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-direction: column;
        flex-direction: column;
    }

    .btn-close {
        border: none;
        font-size: 20px;
        padding: 20px;
        cursor: pointer;
        font-weight: bold;
        color: #4AAE9B;
        background: transparent;
    }
    .btn-close:hover {
        color: #ff3131;
    }
</style>