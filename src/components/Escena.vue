<template>
    <ul>
        <li v-for="item, id in story" :key="id" :class="{ highlighted: item.id === currentSentence}">
                {{item.sentence}}
                <img v-show="currentSentence === item.id" :src="item.img" :alt="item.name">
        </li>
    </ul>
    <div>
    </div>
</template>

<script>
export default {
    props: ['story', 'currentSentence'],
}
</script>   

<style>

img {
    position: absolute;
    top: 0;
    left: 0;

    z-index: -3;
    width: 100vw;
    height: 100vh;

    object-fit: cover; 
}

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