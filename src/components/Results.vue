<template>
    <div class="results">
        <h2>Reaction Time: {{ score }} ms</h2>
        <h1 class="rank"> {{ rank }}</h1>
    </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = "Ninja Fingers"
        } else if (this.score < 400) {
            this.rank = "Rapid Reflexes"
        } else {
            this.rank = "Snail paced..."
        }}}

</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>