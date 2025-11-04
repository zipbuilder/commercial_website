<script lang="ts">
    type Status = 'idle' | 'success';
  let submitStatus: Status = $state('idle');
</script>

<div class="waitlist-form">
  <h2>Join the Waitlist</h2>
  <p class="subtitle">Be the first to experience the future of appliance installation management.</p>

  {#if submitStatus === 'success'}
    <div class="success-message">
      <svg width="48" height="48" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="12" cy="12" r="10" fill="var(--color-success)" opacity="0.2"/>
        <path d="M8 12L11 15L16 9" stroke="var(--color-success)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
      <h3>You're on the list!</h3>
      <p>We'll notify you as soon as ZipBuilder AIMS launches.</p>
    </div>
  {:else}
    <form 
      name="waitlist" 
      method="POST" 
      data-netlify="true"
      action="/success"
    >
      <input type="hidden" name="form-name" value="waitlist" />
      
      <div class="form-group">
        <label for="name">Full Name *</label>
        <input
          type="text"
          id="name"
          name="name"
          placeholder="John Smith"
          required
        />
      </div>

      <div class="form-group">
        <label for="email">Email Address *</label>
        <input
          type="email"
          id="email"
          name="email"
          placeholder="john@example.com"
          required
        />
      </div>

      <div class="form-group">
        <label for="company">Company Name (Optional)</label>
        <input
          type="text"
          id="company"
          name="company"
          placeholder="ABC Appliance Installation"
        />
      </div>

      <button type="submit">
        Join Waitlist
      </button>

      <p class="privacy-notice">
        We respect your privacy. No spam, unsubscribe anytime.
      </p>
    </form>
  {/if}
</div>

<style>
  .waitlist-form {
    width: 100%;
  }

  .waitlist-form h2 {
    color: var(--color-text-primary);
    margin-bottom: 0.5rem;
    font-size: 2rem;
  }

  .subtitle {
    color: var(--color-text-secondary);
    margin-bottom: 2rem;
    font-size: 1rem;
  }

  .form-group {
    margin-bottom: 1.5rem;
  }

  label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 600;
    color: var(--color-text-primary);
    font-size: 0.9rem;
  }

  button {
    width: 100%;
    margin-top: 1rem;
    padding: 1rem;
    font-size: 1.125rem;
  }

  .privacy-notice {
    text-align: center;
    font-size: 0.85rem;
    color: var(--color-text-secondary);
    margin-top: 1rem;
  }

  .success-message {
    text-align: center;
    padding: 2rem 1rem;
  }

  .success-message svg {
    margin-bottom: 1rem;
  }

  .success-message h3 {
    color: var(--color-success);
    margin-bottom: 0.5rem;
  }

  .success-message p {
    color: var(--color-text-secondary);
  }

</style>
