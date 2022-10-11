<template>
    <div :style="{backgroundImage : 'url(../assets/1.jpg)'}">
        content
    </div>
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

    data(){ 
        return {
            image: { 
                // backgroundColor: 'darkorange',
                backgroundImage: 'url("https://sprint6/src/assets/1.jpg")',
                width: '100vw'
            }
            // images: [
            //     {img: '../assets/1.jpg', id: 1},
            //     {img: '../assets/2.jpg', id: 2},
            //     {img: '../assets/3.jpg', id: 3},
            //     {img: '../assets/4.jpg', id: 4},
            // ],  
        }
    },
    props: ['story', 'images', 'currentSentence', 'showContent']
}
</script>   

<style>

.images {
    max-width: 100vw;
    min-width: 100vw;
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