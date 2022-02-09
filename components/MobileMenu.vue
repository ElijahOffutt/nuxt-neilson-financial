<template>
    <v-dialog v-model="show" fullscreen>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis nesciunt cupiditate ea aliquid, quis atque! Vitae exercitationem labore, explicabo ullam officiis numquam, aperiam laboriosam dolor quod inventore tenetur rerum praesentium.</p>
    </v-dialog>
</template>

<script>
export default {
    data(){return{
        show: false
    }},
    mounted(){
        this.$nuxt.$on('showMobileMenu', null, () => { this.show = true })
    }
}
</script>