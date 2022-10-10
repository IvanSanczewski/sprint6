<template>
    <ul>
        <!-- <li v-for="item in story" :key="item" :ref="highlighted"> -->
        <li v-for="item, id in story" :key="id" :class="{ highlighted: (id + 1) === currentSentence}">
            {{item.sentence}}
        </li>
    </ul>
</template>

<script>
// import Home from './Home.vue'

export default {

    // data(){ 
    //     return {
    //         sentenceStart: 'Our hero was surfing the Space when suddenly… he spotted a spaceship!',
    //     }
    // },
    props: ['story', 'currentSentence', 'showContent']

}
</script>   

<style>
ul {
    list-style: none;
    padding-inline-start: 0;
}

li {
    margin: 1em 1em;
    padding: .5em 0;
    
    border: 2px solid black;
    border-radius: 1.5em;
}

.highlighted {
    background: rgb(255,192,203);
}
</style>