<script>

export default {
    name: 'AppContent',
}
</script>

<template>
    <div id="content">
        <h2>Content goes here</h2>
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
