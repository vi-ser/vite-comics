<script>

export default {
    name: 'HeroItem',
}
</script>

<template>
    <div class="hero">
    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

.hero {
    height: 400px;

    background-image: url('img/jumbotron.jpg');
    background-position-x: center;
}
</style>
