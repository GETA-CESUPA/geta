<template>
  <div>
    <nuxt/>
  </div>
</template>

<script>

export default {
  
}
</script>

<style>
/* 
PrimaryColor: "#26A69A"
SecondColor: "#598CFF" */
@import url('https://fonts.googleapis.com/css?family=Montserrat&display=swap');
html {
  scroll-behavior: smooth;
}
body{
  margin: 0;
  padding: 0;
  font-family: 'Montserrat', sans-serif;
}

/* width */
::-webkit-scrollbar {
  width: 3px;
  height: 5px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #fff; 
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: #6d6d6d;
   
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #242424; 
}

.page-enter-active, .page-leave-active {
  transition: opacity .5s;
}
.page-enter, .page-leave-active {
  opacity: 0;
}
</style>

