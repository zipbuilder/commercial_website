<script lang="ts">
  import GasStoveIcon from './assets/appliances/010-gas-stove.png'

  const features = [
    {
      icon: '⏱️',
      title: 'GPS Time Tracking',
      description: 'Accurately track installation time and labor costs across multiple projects using mobile GPS location.'
    },
    {
      icon: GasStoveIcon,
      isImage: true,
      title: 'Installation Management',
      description: 'Monitor appliance installations from delivery to completion with real-time updates from installers.'
    },
    {
      icon: '🔧',
      title: 'Blocker Tracking',
      description: 'Document, report and resolve blockers efficiently with photo uploads, notes and statuses that automatically keep contractors and retailers informed.'
    },
    {
      icon: '💰',
      title: 'Billing Statements',
      description: 'Generate professional invoices and billing statements with automated calculations.'
    },
    {
      icon: '🔄️',
      title: 'Contractor & Retailer Synchronization',
      description: 'Automatically coordinate complex high-rise building projects between contractors and retailers.'
    },
    {
      icon: '📱',
      title: 'Mobile Ready',
      description: 'Access all features on-site with our mobile-optimized interface.'
    }
  ]
</script>

<section class="features">
  <div class="container">
    <div class="section-header">
      <h2>Everything You Need to Streamline Operations</h2>
      <p>Built specifically for appliance installation contractors and commercial retailers</p>
    </div>

    <div class="features-grid">
      {#each features as feature}
        <div class="feature-card">
          <div class="feature-icon">
            {#if feature.isImage}
              <img src={feature.icon} alt={feature.title} class="icon-image" />
            {:else}
              {feature.icon}
            {/if}
          </div>
          <h3>{feature.title}</h3>
          <p>{feature.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .features {
    padding: 5rem 1rem;
    background-color: var(--color-light);
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
  }

  .section-header {
    text-align: center;
    margin-bottom: 4rem;
  }

  .section-header h2 {
    margin-bottom: 1rem;
  }

  .section-header p {
    font-size: 1.25rem;
    color: var(--color-text-secondary);
  }

  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2rem;
  }

  .feature-card {
    background-color: var(--color-white);
    padding: 2rem;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
  }

  .feature-icon {
    font-size: 3rem;
    margin-bottom: 1rem;
  }

  .icon-image {
    height: 60px;
    width: 60px;
    object-fit: contain;
  }

  .feature-card h3 {
    color: var(--color-primary);
    margin-bottom: 0.75rem;
    font-size: 1.5rem;
  }

  .feature-card p {
    color: var(--color-text-secondary);
    line-height: 1.6;
  }

  @media (max-width: 768px) {
    .features {
      padding: 3rem 1rem;
    }

    .features-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
