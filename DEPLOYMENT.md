# Deployment Guide

This guide provides step-by-step instructions for deploying the Portuguese Slave Marriage Records Collection to various platforms.

## GitHub Pages Deployment

### Automatic Deployment (Recommended)

1. **Fork the Repository**

   - Go to the GitHub repository
   - Click "Fork" to create your own copy

2. **Enable GitHub Pages**

   - Go to Settings > Pages
   - Source: Deploy from a branch
   - Branch: `gh-pages` (will be created automatically)
   - Folder: `/ (root)`

3. **Configure GitHub Actions**

   - The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`)
   - This will automatically build and deploy the site when you push to the main branch

4. **Access Your Site**
   - Your site will be available at: `https://yourusername.github.io/repository-name`

### Manual Deployment

If you prefer manual deployment:

```bash
# Clone your repository
git clone https://github.com/yourusername/your-repo.git
cd your-repo

# Install dependencies
bundle install

# Build the site
bundle exec jekyll build

# Deploy to gh-pages branch
bundle exec jekyll build --destination ../site
cd ../site
git init
git add .
git commit -m "Deploy site"
git branch -M gh-pages
git remote add origin https://github.com/yourusername/your-repo.git
git push -f origin gh-pages
```

## Vercel Deployment

1. **Connect Repository**

   - Go to [vercel.com](https://vercel.com)
   - Sign in with GitHub
   - Click "New Project"
   - Import your repository

2. **Configure Build Settings**

   - Framework Preset: Jekyll
   - Build Command: `bundle exec jekyll build`
   - Output Directory: `_site`
   - Install Command: `bundle install`

3. **Deploy**
   - Click "Deploy"
   - Your site will be available at the provided Vercel URL

## Netlify Deployment

1. **Connect Repository**

   - Go to [netlify.com](https://netlify.com)
   - Sign in with GitHub
   - Click "New site from Git"
   - Choose your repository

2. **Configure Build Settings**

   - Build command: `bundle exec jekyll build`
   - Publish directory: `_site`
   - Ruby version: `3.1` (or latest)

3. **Deploy**
   - Click "Deploy site"
   - Your site will be available at the provided Netlify URL

## Environment Variables

For all platforms, you may want to set these environment variables:

- `JEKYLL_ENV`: `production`
- `BUNDLE_WITHOUT`: `development`

## Custom Domain

To use a custom domain:

### GitHub Pages

1. Add your domain to the repository settings
2. Create a `CNAME` file with your domain name
3. Configure DNS records with your domain provider

### Vercel/Netlify

1. Go to Domain settings in your dashboard
2. Add your custom domain
3. Configure DNS records as instructed

## Troubleshooting

### Common Issues

1. **Build Failures**

   - Check Ruby version compatibility
   - Ensure all dependencies are installed
   - Verify Jekyll configuration

2. **Images Not Loading**

   - Check image paths in metadata
   - Ensure images are in the correct directory
   - Verify IIIF configuration

3. **Search Not Working**
   - Run `bundle exec rake wax:search` to regenerate search index
   - Check search configuration in `_config.yml`

### Support

For technical issues:

- Check the [WAX documentation](https://minicomp.github.io/wiki/wax/)
- Review Jekyll and GitHub Pages documentation
- Check the repository issues for known problems
