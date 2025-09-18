# 🌐 AgriScope Website - Cloudflare Pages Deployment Guide

This guide will help you deploy your AgriScope website to Cloudflare Pages for fast, global performance.

## 📋 Prerequisites

- A GitHub account
- A Cloudflare account (free at [cloudflare.com](https://cloudflare.com))
- Git installed on your local machine

## 🚀 Quick Deployment (Recommended)

### Method 1: Deploy from GitHub (Easiest)

1. **Push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: AgriScope website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/agriscope-website.git
   git push -u origin main
   ```

2. **Deploy on Cloudflare Pages**:
   - Go to [dash.cloudflare.com](https://dash.cloudflare.com) and sign in
   - Navigate to "Pages" in the sidebar
   - Click "Create a project"
   - Connect your GitHub account
   - Select your repository
   - Configure build settings:
     - **Framework preset**: None (Static Site)
     - **Build command**: (leave empty)
     - **Build output directory**: (leave empty)
   - Click "Save and Deploy"

3. **Your site will be live** at `https://your-project-name.pages.dev`

### Method 2: Deploy with Wrangler CLI

1. **Install Wrangler CLI**:
   ```bash
   npm install -g wrangler
   ```

2. **Login to Cloudflare**:
   ```bash
   wrangler login
   ```

3. **Deploy**:
   ```bash
   cd /path/to/AgriScopeWeb
   npx wrangler pages deploy
   ```

4. **Follow the prompts**:
   - Choose your account
   - Create new project or link existing
   - Deploy!

## ⚙️ Configuration Files Added

### `wrangler.toml`
- Cloudflare Pages configuration
- Environment settings
- Build output directory settings

### `_headers`
- Security headers (XSS protection, content type options)
- Caching headers for performance
- Permissions policy settings

### `_redirects`
- URL redirects and rewrites
- Currently empty (no redirects needed)

### `package.json` (Updated)
- Wrangler CLI scripts
- Cloudflare Pages deployment commands
- Updated homepage URL

## 🔧 Custom Domain Setup

1. **In Cloudflare Dashboard**:
   - Go to your Pages project
   - Navigate to "Custom domains"
   - Click "Set up a custom domain"
   - Enter your domain name

2. **DNS Configuration**:
   - Cloudflare will automatically configure DNS
   - Or manually add CNAME record pointing to your Pages URL

## 📊 Performance Optimizations

Cloudflare Pages includes:

- **Global CDN**: 200+ data centers worldwide
- **Automatic HTTPS**: SSL certificates included
- **Brotli compression**: Advanced compression
- **HTTP/3 support**: Latest protocol
- **Edge caching**: Intelligent caching at edge locations

## 🔄 Continuous Deployment

Once connected to GitHub:
- Every push to `main` branch = automatic deployment
- Preview deployments for pull requests
- Instant rollbacks if needed
- Branch-based deployments

## 🛠️ Environment Variables

To add environment variables:

1. **In Cloudflare Dashboard**:
   - Go to your Pages project
   - Navigate to "Settings" → "Environment variables"
   - Add your variables

2. **In code**:
   ```javascript
   const apiKey = process.env.API_KEY;
   ```

## 📱 Build Settings

For custom build settings:

```toml
# wrangler.toml
[env.production]
pages_build_output_dir = "."
compatibility_date = "2024-01-01"

# Custom build command (if needed)
# build_command = "npm run build"
```

## 🚨 Troubleshooting

### Common Issues:

1. **Build Fails**:
   - Check `wrangler.toml` syntax
   - Ensure all dependencies are listed in `package.json`

2. **404 Errors**:
   - Verify `_redirects` file
   - Check file paths are correct

3. **Slow Loading**:
   - Images should be optimized
   - Check caching headers in `_headers`

### Debug Commands:

```bash
# Test locally
npx wrangler pages dev

# Check deployment logs
wrangler pages deployment list

# Inspect deployment
wrangler pages deployment tail
```

## 📈 Analytics & Monitoring

Cloudflare provides:
- **Web Analytics** (page views, performance)
- **Core Web Vitals** (LCP, FID, CLS)
- **Real User Monitoring** (RUM)
- **Security analytics**

Enable in project settings → Analytics

## 🔒 Security Features

- **DDoS protection** (automatic)
- **WAF (Web Application Firewall)**
- **Bot management**
- **Security headers** (configured in `_headers`)
- **Zero-trust security** (optional)

## 💰 Pricing

- **Free Plan**: Unlimited bandwidth, 500 builds/month
- **Pro Plan**: $20/month for advanced features
- **Business Plan**: $200/month for enterprise features

## 🎯 Cloudflare-Specific Features

### Workers Integration
- Add serverless functions with Cloudflare Workers
- Edge computing capabilities
- Global function execution

### Image Optimization
- Automatic image optimization
- WebP conversion
- Responsive images

### Speed Optimizations
- **Rocket Loader**: JavaScript optimization
- **Auto Minify**: CSS/JS/HTML minification
- **Mirage**: Mobile image optimization

## 🚀 Advanced Configuration

### Custom Headers
```bash
# _headers file
/*
  X-Frame-Options: DENY
  X-Content-Type-Options: nosniff
  X-XSS-Protection: 1; mode=block

/*.css
  Cache-Control: public, max-age=31536000, immutable
```

### Redirects
```bash
# _redirects file
/old-page /new-page 301
/api/* https://api.example.com/api/:splat 200
```

## 📞 Support

- **Cloudflare Docs**: [developers.cloudflare.com/pages](https://developers.cloudflare.com/pages)
- **Community**: [community.cloudflare.com](https://community.cloudflare.com)
- **Status**: [cloudflarestatus.com](https://cloudflarestatus.com)

## 🎉 Next Steps

After deployment:

1. **Test all functionality**
2. **Set up custom domain**
3. **Configure analytics**
4. **Enable security features**
5. **Share your live site!**

---

🌐 **Your AgriScope website is now powered by Cloudflare's global network!**
