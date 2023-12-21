<script>
  import { onMount } from 'svelte';
  let spanTotal = 25;
</script>


<div class="wrapper">
  <div class="loader"> 
      {#each Array(spanTotal).fill().map((_, index) => index + 1) as i}
         <span style="--i:{spanTotal - i + 1}"></span>
      {/each}
  </div>
</div>


<style>
  :root {
  --background: rgb(45,126,208);
  --gradient: linear-gradient(90deg, rgba(45,126,208,0.8001794467787114) 23%, rgba(167,40,40,1) 92%);
  --skewX: 45deg; 
}
.wrapper {
  transform: translateY(-5rem);
}

  .loader {
    position: relative;
    transform: skewY(-15deg) translateY(50px) translateX(50px);
    animation: animateColor 2.5s linear infinite;
    transform: rotate(80deg); 
  }

  .loader::before {
    content: '';
    position: absolute;
    top: 300px;
    width: 300px;
    height: 200px;
    background: sandybrown;
    transform-origin: bottom;
    transform: skewX(var(--skewX));
    filter: blur(20px);
  }


 span {
  position: relative;
  display: block;
  width: 600px;
  height: 50px;
  background: var(--background);
  background: var(--gradient);
  transition: 0.5s;
  animation: animate 5s ease-in-out infinite;
  animation-delay: calc(-1s * var(--i));
 }
 span:hover {
  background: var(--background);
  transition: 0s;
 }

 span::before {
  content: '';
  position: absolute;
  top: 0;
  left: -25px;
  height: 100%;
  width: 25px;
  background: var(--background);
  background: var(--gradient);
  transform-origin: right;
  transform: skewY(var(--skewX));
  transition: 0.5s;
 }

 span:hover::before {
  background: rgb(31, 35, 38);
  transition: 0s;
 }

 span::after {
  content: '';
  position: absolute;
  top: -25px;
  left: 0;
  width: 100%;
  height: 25px;
  background: red;
  transform-origin: bottom;
  transform: skewX(var(--skewX));
  background: var(--background);
  background: var(--gradient);
 }

 span:hover::after {
  background: rgb(31, 35, 38);
  transition: 0s;
 }


 @keyframes animateColor {
    0% {
      filter: hue-rotate(0deg);
    }
    100% {
      filter: hue-rotate(360deg);
    }
  }


 @keyframes animate {
  0%, 100% {
   transform: translateX(-70px);
  }
  50% {
   transform: translateX(70px);
  }
 }

</style>