<script>
export default {
    name: 'AppNav',

    data() {
        return {
            links: ["characters", "comics", "movies", "tv", "games", "collectibles", "videos", "fans", "news", "shop"],

            activeLinkIndex: 1,
        }
    }
}
</script>

<template>
    <nav>
        <div id="logo-container">
            <img src="/img/dc-logo.png" alt="">
        </div>
        <ul>
            <li v-for="currentLink, index in links" :class="index == activeLinkIndex ? 'active' : ''">
                {{ currentLink }}
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
@use '../styles/variables' as *;

nav {
    display: flex;
    justify-content: space-between;

    height: 118px;
    align-items: center;

    background-color: white;

    padding: 0 $containerPadding;

    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;



    #logo-container {

        display: flex;
        align-items: center;

        img {
            height: 80px;
        }
    }

    ul {
        display: flex;
        gap: 32px;
        color: $secondaryColorLight;

        li {
            list-style-type: none;
            text-transform: uppercase;
            font-size: 14px;
            font-weight: 700;

            &.active {
                color: $primaryColor;
                position: relative;
            }

            &.active::after {
                content: "";
                width: 100%;
                height: 5px;
                background-color: $primaryColor;
                position: absolute;
                top: 64.4px;
                left: 0;
            }

            &:hover {
                cursor: pointer;
            }
        }
    }


}
</style>
