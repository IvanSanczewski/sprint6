<template>
    <div class="nav-btns">
        <button class="btn" @click="previousSentence">Backwards</button>
        <button class="btn" @click="nextSentence">Forward</button>
    </div>
    <Escena :story="story" :currentSentence="currentSentence"/>
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
                {sentence: 'The hero decided to take the door what would take him home.', id: 3},
                {sentence: 'But the other heroes were not so lucky whith their choice.', id: 4 }
            ],
            currentSentence: 1
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
    }

}
</script>

<style>
    button {
        width: 50%;

        padding: 1em 0;
    }
</style>
