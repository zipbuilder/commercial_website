# Netlify Forms Setup Instructions

## After Deploying to Netlify

1. **Enable Form Detection**
   - Netlify automatically detects forms with `data-netlify="true"`
   - Your form is named "waitlist"

2. **View Form Submissions**
   - Go to your Netlify site dashboard
   - Click on "Forms" in the sidebar
   - You'll see all waitlist submissions here

3. **Set Up Email Notifications**
   - In Forms dashboard, click "Form notifications"
   - Click "Add notification"
   - Choose "Email notification"
   - Enter your email address
   - Select "waitlist" form
   - Choose "New form submission" as trigger
   - Save!

4. **Optional Integrations**
   - Slack: Get notified in a Slack channel
   - Webhook: Send data to your own API
   - Zapier: Connect to 1000+ apps

## Form Fields

The waitlist form collects:
- **name** (required) - Full name
- **email** (required) - Email address
- **company** (optional) - Company name

## Success Page

After submission, users are redirected to `/success` which shows:
- Thank you message
- What to expect next
- Link back to home page

## Testing

To test the form locally:
1. Run `npm run dev`
2. Fill out the form
3. Note: Form won't actually submit in dev mode
4. Deploy to Netlify to test live submissions

## Spam Protection

The form includes:
- Hidden honeypot field (Netlify adds automatically)
- reCAPTCHA can be enabled in Netlify dashboard
- Form submission rate limiting

## Download Submissions

From the Netlify Forms dashboard:
- Export as CSV
- Export as JSON
- Integrate with CRM tools
