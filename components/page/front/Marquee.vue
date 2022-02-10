<template>
    <v-carousel >
        <v-carousel-item v-for="(item, i) in items" :key="i">
            <div class="background" :style="`background-image: url('${item.image}')`">
                <div class="content">
                    <p v-for="text in texts" :key="text">{{text}}</p>
                </div>
            </div>
        </v-carousel-item>
    </v-carousel>
</template>

<script>
export default {
    data(){return{
        items: [
            {
                texts: ['Global', 'Protection', 'Specialists'],
                image: 'https://www.neilsonfs.com/media/cmkdaa5d/home-page-1600x515.jpg'
            },
            {
                texts: ['Protecting', 'Customers', 'Is our Aim'],
                image: 'https://www.neilsonfs.com/media/vftid1k5/banner-bg-home-2-1600.jpg'
            }
        ]
    }}
}
</script>