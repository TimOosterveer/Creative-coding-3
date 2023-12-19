<div class="wrapper">
  <div class="loader">
    <span style="--i:17"></span>
    <span style="--i:16"></span>
    <span style="--i:15"></span>
    <span style="--i:14"></span>
    <span style="--i:13"></span>
    <span style="--i:12"></span>
    <span style="--i:11"></span>
    <span style="--i:10"></span>
    <span style="--i:9"></span>
    <span style="--i:8"></span>
    <span style="--i:7"></span>
    <span style="--i:6"></span>
    <span style="--i:5"></span>
    <span style="--i:4"></span>
    <span style="--i:3"></span>
    <span style="--i:2"></span>
    <span style="--i:1"></span>
  </div>
</div>

<style>

.wrapper {
  transform: translateX(-15rem) translateY(-5rem);
}

  .loader {
    position: relative;
    transform: skewY(-15deg) translateY(50px) translateX(50px);
    animation: animateColor 2.5s linear infinite;
    transform: rotate(45deg); 
  }


  .loader::before {
    content: '';
    position: absolute;
    top: 300px;
    width: 300px;
    height: 200px;
    background: sandybrown;
    transform-origin: bottom;
    transform: skewX(45deg);
    filter: blur(20px);
  }


 span {
  position: relative;
  display: block;
  width: 600px;
  height: 50px;
  background: rgb(45,126,208);
  background: linear-gradient(90deg, rgba(45,126,208,0.8001794467787114) 23%, rgba(167,40,40,1) 92%);
  transition: 0.5s;
  z-index: var(--i);
  animation: animate 5s ease-in-out infinite;
  animation-delay: calc(-1s * var(--i));
 }
 span:hover {
  background: rgb(45,126,208); 
  transition: 0s;
 }

 span::before {
  content: '';
  position: absolute;
  top: 0;
  left: -25px;
  height: 100%;
  width: 25px;
  background: rgb(45,126,208);
  background: linear-gradient(90deg, rgba(45,126,208,0.8001794467787114) 23%, rgba(167,40,40,1) 92%);
  transform-origin: right;
  transform: skewY(45deg);
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
  transform: skewX(45deg);
  background: rgb(45,126,208);
  background: linear-gradient(90deg, rgba(45,126,208,0.8001794467787114) 23%, rgba(167,40,40,1) 92%);
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