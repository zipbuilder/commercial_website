<script lang="ts">
  import Hero from './lib/Hero.svelte'
  import Features from './lib/Features.svelte'
</script>

<main>
  <Hero />
  <Features />
  
  <footer>
    <div class="container">
      <p>&copy; 2025 ZipBuilder. All rights reserved.</p>
    </div>
  </footer>
</main>

<style>
  main {
    width: 100%;
  }

  footer {
    background-color: var(--color-dark);
    color: var(--color-text-light);
    padding: 2rem 1rem;
    text-align: center;
  }

  footer .container {
    max-width: 1200px;
    margin: 0 auto;
  }

  footer p {
    color: var(--color-text-light);
  }
</style>
