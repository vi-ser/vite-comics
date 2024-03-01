<script>
export default {
    name: 'AppCta',
    data() {
        return {
            links: [
                '/img/footer-facebook.png',
                '/img/footer-twitter.png',
                '/img/footer-youtube.png',
                '/img/footer-pinterest.png',
                '/img/footer-periscope.png',
            ]
        }
    },
}
</script>

<template>
    <div class="cta">
        <div class="container">

            <div>
                <button>sign-up now!</button>
            </div>


            <div class="links">
                <span>follow us</span>
                <ul>
                    <li v-for="currentLink in links">
                        <img :src="currentLink" alt="">
                    </li>
                </ul>
            </div>

        </div>

    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

.cta {

    background-color: $secondaryColorLight;
    padding: 20px 0;

    button {
        padding: 16px;

        text-transform: uppercase;
        background-color: transparent;

        border: 2px solid $primaryColor;

        font-weight: 700;

        &:hover {
            cursor: pointer;
            background-color: rgba(255, 255, 255, 0.2);
        }

    }

    .container {

        display: flex;
        justify-content: space-between;
        align-items: center;

        .links {

            display: flex;
            gap: 20px;

            span {
                color: $primaryColor;
                text-transform: uppercase;
                font-family: 'Barlow Condensed', sans-serif;
                font-size: 1.3em;
            }

            ul {
                display: flex;
                align-items: center;
                gap: 18px;
                list-style-type: none;

                li:hover {
                    cursor: pointer;
                }

            }
        }
    }
}
</style>
