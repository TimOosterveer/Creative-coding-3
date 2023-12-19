<div>
  <h1>CREAIVE CODING</h1>
</div>

<style>
  div {
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    width: 100%;
    background-color: #461cff;
    color: white;
    animation: pageload 4s ease-in-out forwards; 
    z-index: 1;
    background: rgb(63,173,251);
background: radial-gradient(circle, rgba(63,173,251,0.6741290266106443) 21%, rgba(252,70,70,0.8702074579831933) 100%);
  }

  h1 {
    font-size: 10rem;
    font-weight: 900;
    text-transform: uppercase;
    letter-spacing: 0.5rem;
    animation: h1 4s ease-in-out forwards; 
    filter: blur(1px);
  }

 @keyframes pageload {
  0% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-50vh);
  }

  75% {
    transform: translateY(-25vh);
  }

  90% {
    transform: translateY(-150vh);
  }

  100% {
    transform: translateY(-200vh);
  }
 }

@keyframes h1 {
  0% {
    transform: translateY(0);
  }

  25% {
    transform: translateY(-10vh);
  }

  50% {
    transform: translateY(80vh);
  }

  75% {
    transform: translateY(-100vh);
  }

  100% {
    transform: translateY(-200vh);
  }
}
</style>