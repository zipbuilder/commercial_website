<div class="waitlist-form">
  <h2>Join the Waitlist</h2>
  <p class="subtitle">Be the first to experience the future of appliance installation management.</p>
    <form 
      name="waitlist" 
      method="POST" 
      data-netlify="true"
      action="/success.html"
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
        Not a mailing list. We will only reach out when we launch.
      </p>
    </form>
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
</style>
