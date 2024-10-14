<script>
  import { onMount } from 'svelte';
  import confetti from 'canvas-confetti';

  onMount(() => {
    confetti({
      particleCount: 100,
      spread: 70,
      origin: { y: 0.6 }
    });
  });
</script>

<main class="h-screen flex flex-col items-center justify-center relative overflow-hidden">
  <div class="shifting-background"></div>
  <div class="text-center relative z-10">
    <h1 class="text-6xl md:text-8xl font-birthday text-white mb-8 animate-bounce">
      Happy Birthday
    </h1>
    <h2 class="text-5xl md:text-7xl font-birthday text-yellow-300 animate-pulse">
      Babyyyyyyyyy!
    </h2>
  </div>
  <footer class="absolute bottom-4 text-sm text-white opacity-70 z-10">
    with ❤️ Ar
  </footer>
</main>

<style>
  :global(html, body) {
    height: 100%;
    margin: 0;
    padding: 0;
  }

  .shifting-background {
    position: absolute;
    top: -50%;
    left: -50%;
    right: -50%;
    bottom: -50%;
    width: 200%;
    height: 200%;
    background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
    transform: rotate(0deg);
    z-index: 1;
  }

  @keyframes gradient {
    0% {
      background-position: 0% 50%;
      transform: rotate(0deg);
    }
    50% {
      background-position: 100% 50%;
      transform: rotate(3deg);
    }
    100% {
      background-position: 0% 50%;
      transform: rotate(0deg);
    }
  }
</style>