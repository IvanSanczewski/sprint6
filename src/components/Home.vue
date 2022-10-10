<template>
    <div v-if="!showContent" class="welcome">
        <h2>Welcome to the app, if you're curious about our hero, press start…</h2>
        <button @click="startStory"> START </button>
    </div>
    
    <div v-else>
        <div class="nav-btn">
            <button @click="previousSentence">Backwards</button>
            <button @click="nextSentence">Forward</button>
        </div>
        <Escena :story="story" :currentSentence="currentSentence" :showContent="showContent"/>
    </div>
</template>

<script>
import Escena from './Escena.vue'

export default {
    components: { Escena },
    data () {
        return {
            story: [
                {sentence: 'Our hero was surfing the Space when suddenly… he spotted a spaceship!', id: 1},
                {sentence: 'He felt curious about the spaceship, so he entered in. Once there, he got to a room with two doors.', id: 2},
                {sentence: 'The hero decided to take the door that eventually would take him home.', id: 3},
                {sentence: 'But the other heroes were not so lucky with their choice.', id: 4 }
            ],
            currentSentence: 1,
            showContent: false
        }
    }, 
    methods: {
        previousSentence() {
            if (this.currentSentence !== 1) {
                this.currentSentence --
            }
        },
        nextSentence() {
            if (this.currentSentence !== 4){
                this.currentSentence ++
            }
        },
        startStory() {
            this.showContent = !this.showContent
        }
    }

}
</script>

<style>
    .welcome {
        margin: 0;
        height: 100vh;

        font-family: Avenir, Helvetica, Arial, sans-serif;
        color: white;

        background: rgb(34,124,172);
        background: linear-gradient(100deg, rgba(34,124,172,1) 15%, rgba(17,179,98,1) 100%);
    }
    h2 {
        padding: 5em 3em;
        font-size: xx-large;
    }
    .welcome button {
        margin-top: 2em;

        font-family: Avenir, Helvetica, Arial, sans-serif;
        font-size: x-large;
        font-weight: 700;

        color: blueviolet;
        background: rgb(255,145,0);
        background: linear-gradient(120deg, rgba(255,145,0,1) 20%, rgba(237,0,0,1) 80%);

        border: 4px solid blueviolet;
        border-radius: 1em;

    }

    .nav-btn {
        margin: .5em;
    }
    
    button {
        width: 50%;
        max-width: 433px;
        padding: 1em 0;
    }


</style>
