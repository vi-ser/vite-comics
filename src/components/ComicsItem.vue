<script>
export default {
    name: 'ComicsItem',

    props: {
        comic: Object,
    },
}
</script>

<template>
    <div class="comic">
        <img :src="comic.thumb" alt="">
        <span>{{ comic.series }}</span>
    </div>
</template>

<style lang="scss">
.comic {
    width: calc(100% / 6);
    padding: 14px;

    img {
        width: 100%;
        aspect-ratio: 1;
        object-fit: cover;
        object-position: top;
    }

    span {
        text-transform: uppercase;
        font-size: 0.8em;
    }

    &:hover {
        cursor: pointer;
        background-color: rgba(255, 255, 255, 0.2);
    }
}
</style>