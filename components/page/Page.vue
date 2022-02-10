<template>
    <div class="Page">
        <Header :image="url">
            <slot name="header" />
        </Header>
        <slot name="content" />
    </div>
</template>

<script>
export default {
    props: ['url']
}
</script>

<style lang="scss">
.Content{
    position: relative;
}
</style>