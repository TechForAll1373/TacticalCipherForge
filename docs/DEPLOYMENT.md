# Deployment Guide

This guide explains how to deploy the Tactical Cipher Forge to various static hosting platforms.

## GitHub Pages (Recommended)

The easiest way to host this project is using GitHub Pages, which can be automated with the provided GitHub Actions workflow (`.github/workflows/deploy.yml`).

**Manual Deployment:**
1.  Go to your repository's settings on GitHub.
2.  Navigate to the "Pages" section.
3.  Under "Build and deployment", select the `main` branch as the source and `/ (root)` as the folder.
4.  Click "Save". Your site will be available at `https://<username>.github.io/<repository>`.

## Netlify

1.  Push your code to a GitHub repository.
2.  Sign up for Netlify and drag and drop your repository folder onto the deployment area.
3.  Netlify will automatically detect it as a static site and deploy it.

## Vercel

1.  Install the Vercel CLI: `npm i -g vercel`
2.  Run `vercel` in your project directory.
3.  Follow the prompts to link your project and deploy it.

## Manual Deployment (Any Web Server)

Since this is a static site, you can simply upload the contents of the repository (or just the `index.html`, `style.css`, and `script.js` files) to any web server's public directory (e.g., `/var/www/html` on Apache).
