<template>
    <Escena :prueba="prueba" :story="story"/>
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
            ]
        }
    }

}
</script>

<style>

</style>