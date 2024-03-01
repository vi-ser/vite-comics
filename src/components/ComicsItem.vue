<script>
export default {
    name: 'ComicsItem',

    props: {
        comicsTitle: String,
        comicsImage: String
    },
}
</script>

<template>
    <div class="comic">
        <img :src="comicsImage" alt="">
        <span>{{ comicsTitle }}</span>
    </div>
</template>

<style lang="scss">
.comic {
    width: calc(100% / 6);
    padding: 14px;

    img {
        width: 100%;
        aspect-ratio: 1;
    }

    span {
        text-transform: uppercase;
        font-size: 0.8em;
    }
}
</style>