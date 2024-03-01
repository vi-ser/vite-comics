<script>

import HeroItem from './HeroItem.vue';

export default {
    name: 'AppContent',
    components: {
        HeroItem,
    }
}
</script>

<template>
    <HeroItem></HeroItem>
    <div id="content">
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

#content {
    padding: 56px $containerPadding;
    font-family: 'Barlow Condensed', sans-serif;

    background-color: $secondaryColor;

}
</style>
