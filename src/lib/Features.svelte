<script lang="ts">
  const features = [
    {
      icon: '⏱️',
      title: 'Time Tracking',
      description: 'Accurately track installation time and labor costs across multiple projects and teams.'
    },
    {
      icon: '📦',
      title: 'Installation Tracking',
      description: 'Monitor appliance installations from delivery to completion with real-time updates.'
    },
    {
      icon: '🔧',
      title: 'Defect Management',
      description: 'Document and resolve defects efficiently with photo uploads and status tracking.'
    },
    {
      icon: '💰',
      title: 'Billing Statements',
      description: 'Generate professional invoices and billing statements with automated calculations.'
    },
    {
      icon: '🏢',
      title: 'Project Management',
      description: 'Coordinate complex high-rise building projects with multiple contractors and retailers.'
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
          <div class="feature-icon">{feature.icon}</div>
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
