<template>
   <div class="nav-btn">
        <button @click="previousSentence">Backwards</button>
        <button @click="nextSentence">Forward</button>
    </div>  
</template>

<script>
export default {
    methods: {
        previousSentence() {
            this.$emit('previous')
        },
        nextSentence() {
            this.$emit('next')
        }
    }
}
</script>

<style>
    .nav-btn {
        margin: .5em;
    }
    
    button {
        width: 50%;
        max-width: 433px;
        padding: 1em 0;
        cursor: pointer;
    }
</style>