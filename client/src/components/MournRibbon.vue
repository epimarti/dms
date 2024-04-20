<template>
<span class="ribbon"></span>
</template>
<script>
export default {
  name: 'MournRibbon'
}
</script>

<style>
.ribbon {
  margin: 0;
  padding: 0;
  background: rgb(150, 0, 0);
  color:white;
  padding:0.3em 0;
  position: absolute;
  width: 2.5em;
  top:0;
  left:0;
  transform: translateX(-30%) translateY(0%) rotate(-45deg);
  transform-origin: top right;
}
.ribbon:before,
.ribbon:after {
  content: '';
  position: absolute;
  top:0;
  margin: 0 -1px; /* tweak */
  width: 100%;
  height: 100%;
  background: rgb(150, 0, 0);
}
.ribbon:before {
  right:100%;
}

.ribbon:after {
  left:100%;
}
</style>