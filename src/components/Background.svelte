<!-- src/lib/components/NeonSquaresBackground.svelte -->
<script lang="ts">
    import { onMount, onDestroy } from 'svelte';
    import { browser } from '$app/environment';
 
    let container;
    let squares: { id: number, x: number, y: number }[] = [];
    let isRunning = false;
    const maxSquares = 15;
    const drawInterval = 2000;
    const removeDelay = 6000;
 
    function createSquare() {
      if (!browser || !isRunning || squares.length >= maxSquares) return;
 
      const x = Math.random() * (window.innerWidth - 200);
      const y = Math.random() * (window.innerHeight - 200);
      const newSquare = { id: Date.now(), x, y };
      
      squares = [...squares, newSquare];
 
      // Remove the specific square after animation
      setTimeout(() => {
        squares = squares.filter(square => square.id !== newSquare.id);
      }, removeDelay);
    }
 
    onMount(() => {
      if (browser) {
        isRunning = true;
        const interval = setInterval(createSquare, drawInterval);
        createSquare(); // Start first square immediately
 
        return () => {
          isRunning = false;
          clearInterval(interval);
          squares = []; // Clear all squares on cleanup
        };
      }
    });
</script>
 
<div class="background" bind:this={container}>
  {#each squares as square (square.id)}
    <div
      class="square fade-out"
      style="left: {square.x}px; top: {square.y}px"
    >
      <svg class="pen-line" viewBox="0 0 120 120">
        <path d="M 0 0 L 120 0 L 120 120 L 0 120 L 0 0" />
      </svg>
    </div>
  {/each}
</div>
 
<style>
  .background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #0a0a0a;
    overflow: hidden;
    z-index: -100;
  }
 
  .square {
    position: absolute;
    width: 120px;
    height: 120px;
    transform: rotate(30deg);
  }
 
  .pen-line {
    position: absolute;
    top: 0;
    left: 0;
    width: 120px;
    height: 120px;
    fill: none;
    stroke-width: 2;
    stroke-linecap: round;
    stroke: #fff;
    filter: drop-shadow(0 0 2px #00f7ff)
           drop-shadow(0 0 4px #00f7ff);
    opacity: 0.9;
  }
 
  .pen-line path {
    stroke-dasharray: 480;
    stroke-dashoffset: 480;
    animation: drawPath 4s linear forwards;
  }
 
  @keyframes drawPath {
    to {
      stroke-dashoffset: 0;
    }
  }
 
  .square.fade-out {
    animation: fadeOut 2s forwards;
    animation-delay: 4s;
  }
 
  @keyframes fadeOut {
    to {
      opacity: 0;
    }
  }
</style>