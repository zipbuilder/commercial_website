<script lang="ts">
  import WaitlistForm from './WaitlistForm.svelte'
</script>

<section class="hero">
  <div class="container">
    <div class="hero-content">
      <div class="hero-text">
        <h1>Transform Your Appliance Installation Business</h1>
        <p class="tagline">
          The all-in-one Appliance Installation Management Software (AIMS) designed for contractors and commercial retailers working in residential high-rise projects.
        </p>
        <div class="features-preview">
          <div class="feature-badge">⏱️ Time Tracking</div>
          <div class="feature-badge">📦 Installation Tracking</div>
          <div class="feature-badge">🔧 Defect Management</div>
          <div class="feature-badge">💰 Billing Statements</div>
        </div>
      </div>
      <div class="hero-form">
        <WaitlistForm />
      </div>
    </div>
  </div>
</section>

<style>
  .hero {
    background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-secondary) 100%);
    color: var(--color-white);
    padding: 4rem 1rem;
    min-height: 90vh;
    display: flex;
    align-items: center;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
  }

  .hero-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }

  .hero-text h1 {
    color: var(--color-white);
    margin-bottom: 1.5rem;
  }

  .tagline {
    font-size: 1.25rem;
    color: var(--color-light);
    margin-bottom: 2rem;
    line-height: 1.8;
  }

  .features-preview {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 2rem;
  }

  .feature-badge {
    background-color: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    padding: 0.5rem 1rem;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--color-white);
  }

  .hero-form {
    background-color: var(--color-white);
    padding: 2.5rem;
    border-radius: 16px;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
  }

  @media (max-width: 968px) {
    .hero {
      padding: 3rem 1rem;
      min-height: auto;
    }

    .hero-content {
      grid-template-columns: 1fr;
      gap: 3rem;
    }

    .features-preview {
      justify-content: center;
    }
  }
</style>
