<script>

import HeroItem from './HeroItem.vue';
import ComicsItem from './ComicsItem.vue';
import comicsFile from '../data/dc-comics.json';

export default {
    name: 'AppContent',
    components: {
        HeroItem,
        ComicsItem,
    },

    data() {
        return {

            comicsFile,
        }
    },
}
</script>

<template>
    <HeroItem></HeroItem>
    <div id="content">
        <div class="container">
            <div class="current-series">
                <span>current series</span>
            </div>
            <ComicsItem v-for="currentComics in comicsFile" :comic="currentComics"></ComicsItem>
            <button>load more</button>
        </div>
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

#content {
    background-color: $secondaryColor;

    .container {
        padding: 54px 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        position: relative;

        .current-series {
            position: absolute;

            top: -30px;
            left: 0;

            font-family: 'Barlow Condensed', sans-serif;
            font-size: 2em;
            font-weight: bold;
            text-transform: uppercase;

            padding: 6px 32px;

            background-color: $primaryColor;
            color: white;
        }

        button {
            margin-top: 20px;
            padding: 12px 60px;

            border-radius: 0%;
            border: none;

            font-family: 'Barlow Condensed', sans-serif;
            font-size: 16px;
            font-weight: bold;
            text-transform: uppercase;

            background-color: $primaryColor;

            &:hover {
                cursor: pointer;
                background-color: white;
                color: $primaryColor;
                transition: .3s;
            }

        }
    }

}
</style>
