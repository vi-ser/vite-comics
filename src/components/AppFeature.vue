<script>
export default {
    name: 'AppFeature',
    data() {
        return {
            features: [
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
    <div id="blue-features">
        <div class="container">
            <div class="row">

                <div v-for="currentFeature in features" class="col">
                    <img :src="currentFeature.img" alt="Buy digital comics">
                    <span>{{ currentFeature.text }}</span>
                </div>

            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

#blue-features {
    background-color: $primaryColor;
    text-transform: uppercase;
    font-size: 0.9em;
    font-weight: 500;

    .row {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 60px;

        padding: 50px;

        .col {
            display: flex;
            align-items: center;
            gap: 20px;

            height: 55px;

            span {
                white-space: nowrap;
            }

            img {
                max-width: 55px;
                height: 100%;
            }
        }
    }
}
</style>
