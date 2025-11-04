<script lang="ts">
  import WaitlistForm from './WaitlistForm.svelte'
  import ZBLogo from '../assets/ZB1.png'
  import GasStoveIcon from '../assets/appliances/010-gas-stove.png'
</script>

<section class="header">
  <div class="header-container">
    <div class="header-brand">
      <h1>ZipBuilder</h1>
    </div>
    <div class="header-logo">
      <img src={ZBLogo} alt="ZipBuilder Logo" />
    </div>
  </div>
</section>
<section class="hero">
  <div class="container">
    <div class="hero-content">
      <div class="hero-text">
        <h1>Transform Your Appliance Installation Business</h1>
        <p class="tagline">
          The all-in-one Appliance Installation Management Software (AIMS) designed for contractors and commercial retailers working in residential high-rise projects.
        </p>
        <div class="features-preview">
          <div class="feature-badge">⏱️ GPS Time Tracking</div>
          <div class="feature-badge"><img src={GasStoveIcon} alt="Installation" class="badge-icon" /> Installation Management</div>
          <div class="feature-badge">🔧 Blocker Tracking</div>
          <div class="feature-badge">💰 Billing Statements</div>
          <div class="feature-badge">🔄 Contractor & Retailer Synchronization</div>
        </div>
      </div>
      <div class="hero-form">
        <WaitlistForm />
      </div>
    </div>
  </div>
</section>

<style>
  .header {
    background-color: var(--color-white);
    padding: 1rem;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    position: relative;
  }

  .header-container {
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    padding: 0 1rem;
  }

  .header-brand {
    position: absolute;
    left: 0;
  }

  .header-brand h1 {
    margin: 0;
    font-size: 1.5rem;
    color: var(--color-primary);
    font-weight: 700;
  }

  .header-logo {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .header-logo img {
    height: 50px;
    width: auto;
    object-fit: contain;
  }

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
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .badge-icon {
    height: 18px;
    width: 18px;
    object-fit: contain;
  }

  .hero-form {
    background-color: var(--color-white);
    padding: 2.5rem;
    border-radius: 16px;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
  }

  @media (max-width: 768px) {
    .header-container {
      flex-direction: column;
      gap: 0.5rem;
    }

    .header-brand {
      position: static;
    }

    .header-brand h1 {
      font-size: 1.25rem;
    }

    .header-logo img {
      height: 40px;
    }
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
