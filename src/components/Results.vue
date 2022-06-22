<template>
  <p>Reaction time:{{ score }} ms</p> 
  <p class="rank">{{ rank }}</p>
  
  
</template>

<script>
export default {
props:['score'],

data(){
    return{
        rank: null
    }
},

mounted(){
    if(this.score<100)
    {
        this.rank = 'Ninja Fingers'
    }
    else  if(this.score<200)
    {
        this.rank = 'Rapid Reflexes'
    }
    else
    {
        this.rank = 'Snail Pace...'
    }   
}
}
</script>

<style>
.rank{
     font-size: 1.4em;     
     color: rgb(100, 197, 113);
     font-weight: bold;
    }
</style>