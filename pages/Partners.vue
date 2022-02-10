<template>
    <Page :url="image">
        <template v-slot:header>
            <h1>Our Team</h1>
        </template>
        <template v-slot:content>
            <div class="Content">
                <h2>Meet the Team</h2>
            </div>
        </template>
    </Page>
</template>

<script>
export default {
    data(){return{
        image: this.$nuxt.$baseURL+'/media/u0unwgsq/our-team-1600x515.jpg'
    }}
}
</script>