<script>
export default {
    name: 'AppFeature',
    data() {
        return {
            icons: [
                {
                    img: '/img/buy-comics-digital-comics.png',
                    text: 'digital comics'
                },

                {
                    img: '/img/buy-comics-merchandise.png',
                    text: 'dc merchandise'
                },
                {
                    img: '/img/buy-comics-subscriptions.png',
                    text: 'subscription'
                },
                {
                    img: '/img/buy-comics-shop-locator.png',
                    text: 'comic shop locator'
                },
                {
                    img: '/img/buy-dc-power-visa.svg',
                    text: 'dc power visa'
                },
            ]
        }
    },
}
</script>

<template>
    <section id="icons">
        <div v-for="(currentItem, index) in icons" class="icon-item">
            <img :class="{ 'last-icon': index === icons.length - 1 }" :src="currentItem.img" alt="">
            <span>{{ currentItem.text }}</span>
        </div>
    </section>
</template>

<style lang="scss">
@use '../styles/variables' as *;

#icons {
    display: flex;
    justify-content: center;
    gap: 36px;

    padding: 50px 0;

    background-color: $primaryColor;

    .icon-item {

        display: flex;
        gap: 16px;

        align-items: center;

        font-size: 14px;
        font-weight: 500;

        img {
            height: 55px;
            width: auto;

            &.last-icon {
                width: 55px;
                height: auto;
            }
        }

        span {
            text-transform: uppercase;
        }

    }


}
</style>
