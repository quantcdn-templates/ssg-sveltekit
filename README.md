# SvelteKit Static Site Template

A SvelteKit static site template configured for deployment to QuantCDN.

[![Deploy to QuantCDN](https://www.quantcdn.io/img/quant-deploy-btn-sml.svg)](https://dashboard.quantcdn.io/projects/add/jamstack?template=sveltekit)

## Features

- SvelteKit with `@sveltejs/adapter-static` for static site generation
- TypeScript support
- Svelte 5 with runes
- Automatic deployment to QuantCDN via GitHub Actions
- Global CDN distribution

## Getting Started

### Prerequisites

- Node.js 20 or later
- npm

### Local Development

1. Install dependencies:

```bash
npm install
```

2. Start the development server:

```bash
npm run dev
```

3. Open [http://localhost:5173](http://localhost:5173) in your browser.

### Building for Production

```bash
npm run build
```

The static files will be generated in the `build` directory.

### Preview Production Build

```bash
npm run preview
```

## Deployment to QuantCDN

### Automatic Deployment

This template includes a GitHub Actions workflow that automatically deploys to QuantCDN when you push to the `main` branch.

#### Required Secrets

Configure these secrets in your GitHub repository:

- `QUANT_CUSTOMER` - Your QuantCDN customer ID
- `QUANT_PROJECT` - Your QuantCDN project name
- `QUANT_TOKEN` - Your QuantCDN API token

### Manual Deployment

You can also deploy manually using the [Quant CLI](https://www.quantcdn.io/docs/cli):

```bash
npm install -g @quantcdn/cli
npm run build
quant deploy --dir build
```

## Project Structure

```
ssg-sveltekit/
├── src/
│   ├── app.html         # HTML template
│   ├── app.d.ts         # TypeScript declarations
│   └── routes/
│       ├── +layout.svelte  # Root layout
│       └── +page.svelte    # Home page
├── static/              # Static assets
├── quant/
│   └── meta.json        # QuantCDN template metadata
├── .github/workflows/
│   └── deploy.yml       # CI/CD workflow
├── svelte.config.js     # SvelteKit configuration
├── vite.config.ts       # Vite configuration
├── tsconfig.json        # TypeScript configuration
└── package.json
```

## Resources

- [SvelteKit Documentation](https://svelte.dev/docs/kit)
- [Svelte Documentation](https://svelte.dev/docs/svelte)
- [QuantCDN Documentation](https://www.quantcdn.io/docs)
- [Quant CLI](https://www.quantcdn.io/docs/cli)

## License

MIT
