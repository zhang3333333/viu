<template>
    <div class="peper-cards-image">
        <div style="position: absolute;width: 100%; height: 100%;" v-if="imgSmall !== ''">
            <load-img :img="img" :img-small="imgSmall" v-if="img"></load-img>
        </div>
        <div style="position: absolute;width: 100%; height: 100%;" v-if="imgSmall === ''">
            <img :src="img" alt="" v-if="img">
        </div>
        <div class="peper-cards-image-overlay"></div>
        <slot></slot>
    </div>
</template>

<script>
    export default {
        props: {
            img : {
                default: "",
                type: String,
            },
            imgSmall : {
                default: "",
                type: String,
            }
        }
    }
</script>
