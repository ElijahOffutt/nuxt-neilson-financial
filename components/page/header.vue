<template>
    <v-container fluid>
        <v-row justify="center" align="center" style="height: 400px">
            <v-col style="width: 1200px">
                <h1>{{heading}}</h1>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    props: ['heading']
}
</script>