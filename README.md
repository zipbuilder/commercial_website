# ZipBuilder Landing Page# ZipBuilder Landing Page# Svelte + TS + Vite



A modern, responsive landing page for ZipBuilder's Appliance Installation Management Software (AIMS) with waitlist signup functionality.



## FeaturesA modern, responsive landing page for ZipBuilder's Appliance Installation Management Software (AIMS) with waitlist signup functionality.This template should help get you started developing with Svelte and TypeScript in Vite.



- 🎨 Modern design with orange brand colors

- 📱 Fully responsive layout

- ✉️ Email waitlist signup with Netlify Forms## Features## Recommended IDE Setup

- 🎯 Built with Svelte 5 and TypeScript

- 🚀 Optimized for performance

- 📬 No backend needed - forms handled by Netlify

- 🎨 Modern design with orange brand colors[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Getting Started

- 📱 Fully responsive layout

### Prerequisites

- ✉️ Email waitlist signup with Netlify Functions## Need an official Svelte framework?

- Node.js 18+ 

- npm or yarn- 🎯 Built with Svelte 5 and TypeScript



### Installation- 🚀 Optimized for performanceCheck out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.



```bash

# Install dependencies

npm install## Getting Started## Technical considerations



# Run development server

npm run dev

### Prerequisites**Why use this over SvelteKit?**

# Build for production

npm run build



# Preview production build- Node.js 18+ - It brings its own routing solution which might not be preferable for some users.

npm run preview

```- npm or yarn- It is first and foremost a framework that just happens to use Vite under the hood, not a Vite app.



## Deployment to Netlify



### 1. Push to GitHub### InstallationThis template contains as little as possible to get started with Vite + TypeScript + Svelte, while taking into account the developer experience with regards to HMR and intellisense. It demonstrates capabilities on par with the other `create-vite` templates and is a good starting point for beginners dipping their toes into a Vite + Svelte project.



Make sure your code is pushed to a GitHub repository.



### 2. Connect to Netlify```bashShould you later need the extended capabilities and extensibility provided by SvelteKit, the template has been structured similarly to SvelteKit so that it is easy to migrate.



1. Go to [Netlify](https://netlify.com) and sign in# Install dependencies

2. Click "Add new site" → "Import an existing project"

3. Connect your GitHub repositorynpm install**Why `global.d.ts` instead of `compilerOptions.types` inside `jsconfig.json` or `tsconfig.json`?**

4. Netlify will auto-detect the build settings from `netlify.toml`



### 3. Configure Form Notifications

# Run development serverSetting `compilerOptions.types` shuts out all other types not explicitly listed in the configuration. Using triple-slash references keeps the default TypeScript setting of accepting type information from the entire workspace, while also adding `svelte` and `vite/client` type information.

After deployment:

1. Go to your Netlify site dashboardnpm run dev

2. Navigate to **Forms** → **Form notifications**

3. Add your email to receive notifications when someone joins the waitlist**Why include `.vscode/extensions.json`?**

4. Optionally, integrate with Slack, Discord, or other services

# Build for production

### 4. Deploy

npm run buildOther templates indirectly recommend extensions via the README, but this file allows VS Code to prompt the user to install the recommended extension upon opening the project.

Click "Deploy site" and Netlify will build and deploy your site automatically.



## How Netlify Forms Work

# Preview production build**Why enable `allowJs` in the TS template?**

The form uses `data-netlify="true"` attribute which tells Netlify to automatically handle form submissions. When someone submits:

npm run preview

1. Form data is captured by Netlify

2. User is redirected to `/success` page```While `allowJs: false` would indeed prevent the use of `.js` files in the project, it does not prevent the use of JavaScript syntax in `.svelte` files. In addition, it would force `checkJs: false`, bringing the worst of both worlds: not being able to guarantee the entire codebase is TypeScript, and also having worse typechecking for the existing JavaScript. In addition, there are valid use cases in which a mixed codebase may be relevant.

3. You receive a notification through your Netlify dashboard

4. All submissions are stored in Netlify's Forms dashboard



No serverless functions or email configuration needed!## Deployment to Netlify**Why is HMR not preserving my local component state?**



## Project Structure



```### 1. Push to GitHubHMR state preservation comes with a number of gotchas! It has been disabled by default in both `svelte-hmr` and `@sveltejs/vite-plugin-svelte` due to its often surprising behavior. You can read the details [here](https://github.com/rixo/svelte-hmr#svelte-hmr).

commercial_website/

├── src/

│   ├── lib/

│   │   ├── Hero.svelte           # Hero section with CTAMake sure your code is pushed to a GitHub repository.If you have state that's important to retain within a component, consider creating an external store which would not be replaced by HMR.

│   │   ├── WaitlistForm.svelte   # Email signup form

│   │   └── Features.svelte       # Features showcase

│   ├── App.svelte                # Main app component

│   ├── app.css                   # Global styles with CSS variables### 2. Connect to Netlify```ts

│   └── main.ts                   # App entry point

├── public/// store.ts

│   └── success.html              # Success page after form submission

├── index.html                    # Entry HTML (includes hidden form for Netlify)1. Go to [Netlify](https://netlify.com) and sign in// An extremely simple external store

├── netlify.toml                  # Netlify configuration

└── package.json2. Click "Add new site" → "Import an existing project"import { writable } from 'svelte/store'

```

3. Connect your GitHub repositoryexport default writable(0)

## Customization

4. Netlify will auto-detect the build settings from `netlify.toml````

### Colors



All colors are defined as CSS variables in `src/app.css`:### 3. Configure Form Notifications



```cssAfter deployment:

--color-primary: #FF6B35;      /* Orange from logo */1. Go to your Netlify site dashboard

--color-secondary: #FF8C5A;    /* Lighter orange */2. Navigate to **Forms** → **Form notifications**

--color-accent: #2B5AA6;       /* Blue accent */3. Add your email to receive notifications when someone joins the waitlist

```4. Optionally, integrate with Slack, Discord, or other services



Update these variables to match your brand colors.### 4. Deploy



### ContentClick "Deploy site" and Netlify will build and deploy your site automatically.



- Edit `src/lib/Hero.svelte` to update the hero section text## Project Structure

- Edit `src/lib/Features.svelte` to modify the features list

- Update company name and links in `src/App.svelte` footer```

commercial_website/

## Tech Stack├── src/

│   ├── lib/

- **Frontend**: Svelte 5, TypeScript, Vite│   │   ├── Hero.svelte           # Hero section with CTA

- **Styling**: CSS with custom properties│   │   ├── WaitlistForm.svelte   # Email signup form

- **Forms**: Netlify Forms (built-in form handling)│   │   └── Features.svelte       # Features showcase

│   ├── App.svelte                # Main app component

## License│   ├── app.css                   # Global styles with CSS variables

│   └── main.ts                   # App entry point

Private project for ZipBuilder.├── public/

│   └── success.html              # Success page after form submission
├── netlify.toml                  # Netlify configuration
└── package.json
```

## Customization

### Colors

All colors are defined as CSS variables in `src/app.css`:

```css
--color-primary: #FF6B35;      /* Orange from logo */
--color-secondary: #FF8C5A;    /* Lighter orange */
--color-accent: #2B5AA6;       /* Blue accent */
```

Update these variables to match your brand colors.

### Content

- Edit `src/lib/Hero.svelte` to update the hero section text
- Edit `src/lib/Features.svelte` to modify the features list
- Update company name and links in `src/App.svelte` footer

## Tech Stack

- **Frontend**: Svelte 5, TypeScript, Vite
- **Styling**: CSS with custom properties
- **Forms**: Netlify Forms (built-in form handling)

## License

Private project for ZipBuilder.
