<template>
    <ul>
        <li v-for="item in story" :key="item" class="">
            {{item.sentence}}
        </li>
        <!-- <h4> {{ story.sentence }}</h4> -->
    </ul>
    <!-- <p>{{ sentenceStart }}</p> -->

</template>

<script>
// import Home from './Home.vue'

export default {
    // component: { Home },
    data(){ 
        return {
            sentenceStart: 'Our hero was surfing the Space when suddenly… he spotted a spaceship!',
            //  story: [
            //     {sentence: 'Our hero was surfing the Space when suddenly… he spotted a spaceship!', id: 1},
            //     {sentence: 'He felt curious about the spaceship, so he entered in. Once there, he got to a room with two doors.', id: 2},
            //     {sentence: 'The hero decided to take the door what would take him home.', id: 3},
            //     {sentence: 'But the other heroes were not so lucky whith their choice.', id: 4 }
            // ]
        }
    },
    props: ['story']

}
</script>   

<style>
ul {
    list-style: none;
}

li {
    margin: 1em 0;
    padding: .5em 0;
    
    border: 2px solid black;
    border-radius: 1.5em;
}

</style>