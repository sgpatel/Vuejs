<template>
<div>
    <p>Reaction Time: {{score}} ms</p>
    <p class="rank">My Rank :{{rank}}</p>
</div>
</template>

<script>
export default {
    props:['score'],
    data(){
        return{
            rank : null
        }
    },

    mounted(){
        if(this.score<2500){
            this.rank = 'Ninja Fingers'
        }else if(this.score<4000){
            this.rank = 'Rapid Reflex'

        }else{
            this.rank='snail pace...'
        }
    }

}
</script>

<style>
.rank {
font-size:1.4em;
color: #0faf87;
font-weight: bold;

}
</style>