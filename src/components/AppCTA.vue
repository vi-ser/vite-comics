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
</template>

<style lang="scss">
@use '../styles/variables' as *;

.cta {

    display: flex;
    justify-content: space-between;
    align-items: center;

    background-color: $secondaryColorLight;
    padding: 30px $containerPadding;

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

    .links {

        display: flex;
        align-items: center;

        span {
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            font-weight: 700;
            color: $primaryColor;
            text-transform: uppercase;
        }

        ul {
            display: flex;
            gap: 20px;

            li {
                list-style-type: none;

                &:hover {
                    cursor: pointer;
                }
            }
        }
    }
}
</style>
