# Imgix Setup Guide

## Step 1: Connect GitHub Repository to Imgix

1. Log in to your Imgix dashboard
2. Click "Add Source"
3. Select "Web Folder" as Source Type
4. Enter your GitHub repository URL in the "Base URL" field
   - Format: `https://raw.githubusercontent.com/yourusername/your-repo-name/main/`
   - Example: `https://raw.githubusercontent.com/username/shared-images/main/`

## Step 2: Configure Imgix Subdomains

1. Under "Domains" section, set up your Imgix subdomain
   - Add a custom subdomain like `images.yourdomain.com`
   - Or use the default Imgix subdomain (e.g., `your-source.imgix.net`)

2. For multiple websites, use the same Imgix source but with different paths:
   - Website 1: `https://your-source.imgix.net/images/seaqdecksandpatios/image.jpg`
   - Website 2: `https://your-source.imgix.net/images/another-site/image.jpg`

## Step 3: Asset Manager Settings

1. Select "Include All Paths" for Asset Processing Rule
2. Add any specific rules you need for image processing

## Step 4: Using Imgix URLs in Your Websites

Example usage:

```html
<!-- Basic image -->
<img src="https://your-source.imgix.net/images/seaqdecksandpatios/deck.jpg" alt="Deck">

<!-- Resized image -->
<img src="https://your-source.imgix.net/images/seaqdecksandpatios/deck.jpg?w=600&h=400&fit=crop" alt="Deck">

<!-- Optimized for web -->
<img src="https://your-source.imgix.net/images/seaqdecksandpatios/deck.jpg?auto=format,compress" alt="Deck">
```

## Step 5: Set up Custom Domain (Optional)

For a more branded experience, you can set up a custom domain:

1. Create a CNAME record in your DNS settings pointing to `your-source.imgix.net`
2. Add the custom domain in your Imgix source settings

## Parameter Defaults

Consider setting these parameter defaults for optimal performance:

- `auto=format` - automatically serves the best format for the browser
- `q=75` - sets a good balance between quality and file size 