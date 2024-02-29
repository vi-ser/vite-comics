<script>
export default {
    name: 'AppFooter',
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
    <footer>
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
    </footer>
</template>

<style lang="scss">
@use '../styles/variables' as *;

footer {
    display: flex;
    justify-content: space-between;

    height: 345px;
    padding: 40px $containerPadding;
    background-image: url('/img/footer-bg.jpg');
    background-size: cover;

    overflow: hidden;


    .links {

        display: flex;
        flex-direction: column;
        column-gap: 32px;
        flex-wrap: wrap;

        .links-list {

            z-index: 1;

            h3 {
                font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

                margin-bottom: 12px;
            }

            ul {

                padding: 0;
                margin-bottom: 24px;

                li {
                    list-style-type: none;
                    color: #959595;
                    font-size: 14px;

                    &:hover {
                        color: white;
                        cursor: pointer;
                    }
                }


            }

        }
    }

    img {
        transform: scale(1.5);
    }

}
</style>
