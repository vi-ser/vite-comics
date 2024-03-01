<script>
import AppFeature from './AppFeature.vue';

export default {
    name: 'AppFooter',

    components: {
        AppFeature,
    },

    data() {
        return {
            links: [
                {
                    title: "DC COMICS",
                    list: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    title: "SHOP",
                    list: [
                        'Shop DC',
                        'Shop Collectibles',
                    ]
                },
                {
                    title: "DC",
                    list: [
                        'Terms Of Use',
                        'Privacy policy (New)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us',
                    ]
                },
                {
                    title: "SITES",
                    list: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa',
                    ]
                },

            ]

        }
    },
}

</script>

<template>
    <AppFeature></AppFeature>
    <footer>
        <div class="container">
            <div class="links">
                <div v-for="linkList in links" class="links-list">
                    <h3>{{ linkList.title }}</h3>
                    <ul>
                        <li v-for="currentLink in linkList.list">
                            {{ currentLink }}
                        </li>
                    </ul>
                </div>
            </div>
            <img src="/img/dc-logo-bg.png" alt="">
        </div>
    </footer>
</template>

<style lang="scss">
@use '../styles/variables' as *;

footer {

    height: 370px;

    background-image: url('/img/footer-bg.jpg');
    background-position: cover;

    overflow: hidden;

    ul {
        list-style: none;
        margin-bottom: 12px;
        padding: 0;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        height: 100%;
    }


    .links {

        display: flex;
        flex-flow: column wrap;
        align-content: flex-start;
        gap: 20px 30px;

        height: 100%;

        padding: 40px 0;

        .links-list {

            z-index: 1;

            h3 {
                text-transform: uppercase;
                font-family: 'Barlow Condensed', sans-serif;

                margin-bottom: 10px;
            }

            ul {

                li {
                    color: #959595;
                    font-size: 12px;

                    &:hover {
                        color: white;
                        cursor: pointer;
                    }
                }
            }
        }
    }

}
</style>
