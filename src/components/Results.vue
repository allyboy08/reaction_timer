<template>
  <p>Reaction time - {{score}} ms</p>
  <p class="rank"> {{rank}}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return{
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Yellow flash'
        } else if (this.score < 400) {
            this.rank = 'Usain bolt'
        } else {
            this.rank = 'Your weak'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>