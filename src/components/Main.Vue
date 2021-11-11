<template>
<main>
    <div class="container">
        <div class="jumbotron">
            <h1>--> Content goes here -- </h1>
        </div>
        
    </div>
</main>
</template>

<script>

export default {
  name:"Main"
}
</script>

<style lang="scss" scoped>
    @import "../style/variables";
    
    main{
        background-color:$bg-dark;
    }
    
    .container{
        margin: 0 auto;
        width: $w-75;
        background-color:black;

        .jumbotron{
            padding: $padding-containers-y $padding-containers-x; 
        }
    }
    h1{
        color:white
    }
</style>