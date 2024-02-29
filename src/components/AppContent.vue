<script>

import AppFeature from './AppFeature.vue';

export default {
    name: 'AppContent',
    components: { AppFeature }
}
</script>

<template>
    <div id="content">
        <h2>Content goes here</h2>
    </div>
    <AppFeature></AppFeature>
</template>

<style lang="scss">
@use '../styles/variables' as *;

#content {
    padding: 56px $containerPadding;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;

    background-color: $secondaryColor;

}
</style>
