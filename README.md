# Return To Her - Hugo Blog

A personal blog built with Hugo, designed to be hosted on GitHub Pages. This blog focuses on personal growth, mindfulness, and returning to what truly matters in life.

## Features

- Clean, modern design with responsive layout
- Built-in navigation menu
- Blog post listing with excerpts
- Tag support for posts
- Optimized for GitHub Pages hosting
- Mobile-friendly design

## Local Development

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (Extended version recommended)
- Git

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/sfraney/ReturnToHer.git
   cd ReturnToHer
   ```

2. Start the Hugo development server:
   ```bash
   hugo server -D
   ```

3. Open your browser and navigate to `http://localhost:1313`

### Building for Production

To build the site for production:

```bash
hugo --minify
```

This will generate the static files in the `public/` directory.

## GitHub Pages Deployment

### Option 1: GitHub Actions (Recommended)

1. Create a `.github/workflows/hugo.yml` file in your repository:

```yaml
name: Deploy Hugo site to Pages

on:
  push:
    branches: ["main"]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

defaults:
  run:
    shell: bash

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb
          sudo dpkg -i ${{ runner.temp }}/hugo.deb
        env:
          HUGO_VERSION: 0.121.1
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
          fetch-depth: 0
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v4
      - name: Build with Hugo
        env:
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --gc \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

2. In your GitHub repository settings:
   - Go to Settings → Pages
   - Set Source to "GitHub Actions"

### Option 2: Manual Deployment

1. Build the site locally:
   ```bash
   hugo --minify
   ```

2. Create a `gh-pages` branch and push the `public/` directory:
   ```bash
   git checkout -b gh-pages
   git add public/
   git commit -m "Deploy to GitHub Pages"
   git push origin gh-pages
   ```

3. In your GitHub repository settings:
   - Go to Settings → Pages
   - Set Source to "Deploy from a branch"
   - Select the `gh-pages` branch and `/ (root)` folder

## Configuration

### Site Settings

Edit `config.toml` to customize your site:

- `baseURL`: Update with your actual GitHub Pages URL
- `title`: Your site title
- `params.description`: Site description
- `params.author`: Your name

### Adding Content

- **Pages**: Add markdown files to `content/`
- **Blog Posts**: Add markdown files to `content/blog/`
- **Images**: Place images in `static/` directory

### Front Matter

Blog posts should include front matter:

```yaml
---
title: "Your Post Title"
date: 2024-01-15
tags: ["tag1", "tag2"]
summary: "Brief description of the post"
---
```

## Customization

### Styling

The site uses inline CSS for simplicity. To customize the design:

1. Edit the `<style>` sections in the template files
2. Modify colors, fonts, and layout in `layouts/_default/baseof.html`

### Adding Features

- **Comments**: Integrate Disqus or other comment systems
- **Analytics**: Add Google Analytics or other tracking
- **Search**: Implement search functionality
- **Categories**: Add category support beyond tags

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Feel free to submit issues and enhancement requests!

---

*Built with [Hugo](https://gohugo.io/) and hosted on [GitHub Pages](https://pages.github.com/)* 