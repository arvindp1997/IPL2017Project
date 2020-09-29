<template>
    <div class="match">
       <div  v-bind:key="match.id" v-for="match in matches">
         <MatchItem v-bind:match="match"/>

       </div>
    </div>
</template>

<script>
import MatchItem from './MatchItem.vue';
export default {
    name:"IPL Matches stats",
    components:{
        MatchItem
    }
    ,
    props:["matches"]
}
</script>

<style scoped>
 .match {
  background-color: #eec0c6;
background-image: linear-gradient(315deg, #eec0c6 0%, #7ee8fa 74%);
;

 }
</style>