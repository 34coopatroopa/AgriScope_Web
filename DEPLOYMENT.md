# 🚀 AgriScope Website - Vercel Deployment Guide

This guide will help you deploy your AgriScope website to Vercel in just a few steps.

## 📋 Prerequisites

- A GitHub account
- A Vercel account (free at [vercel.com](https://vercel.com))
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

2. **Deploy on Vercel**:
   - Go to [vercel.com](https://vercel.com) and sign in
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will automatically detect it's a static site
   - Click "Deploy"

3. **Your site will be live** at `https://your-project-name.vercel.app`

### Method 2: Deploy with Vercel CLI

1. **Install Vercel CLI**:
   ```bash
   npm install -g vercel
   ```

2. **Deploy**:
   ```bash
   cd /path/to/AgriScopeWeb
   vercel
   ```

3. **Follow the prompts**:
   - Link to existing project or create new
   - Choose your team/account
   - Deploy!

## ⚙️ Configuration Files Added

### `package.json`
- Defines project metadata and scripts
- Includes Vercel-specific scripts
- Sets up proper dependencies

### `vercel.json`
- Configures Vercel deployment settings
- Sets up caching headers for performance
- Defines security headers
- Routes all requests to static files

### `.gitignore` & `.vercelignore`
- Excludes unnecessary files from deployment
- Keeps repository clean

## 🔧 Custom Domain Setup

1. **In Vercel Dashboard**:
   - Go to your project settings
   - Navigate to "Domains"
   - Add your custom domain

2. **DNS Configuration**:
   - Add CNAME record pointing to `cname.vercel-dns.com`
   - Or add A records for Vercel IPs

## 📊 Performance Optimizations

The deployment includes:

- **Static file caching** (1 year for CSS/JS/images)
- **Security headers** (XSS protection, content type options)
- **Gzip compression** (automatic)
- **CDN distribution** (global edge network)

## 🔄 Continuous Deployment

Once connected to GitHub:
- Every push to `main` branch = automatic deployment
- Preview deployments for pull requests
- Instant rollbacks if needed

## 🛠️ Environment Variables (if needed)

If you add environment variables later:

1. **In Vercel Dashboard**:
   - Go to project settings
   - Navigate to "Environment Variables"
   - Add your variables

2. **In code**:
   ```javascript
   const apiKey = process.env.REACT_APP_API_KEY;
   ```

## 📱 Custom Build Settings

The site is configured as a static site, but you can customize:

```json
{
  "buildCommand": "npm run build",
  "outputDirectory": "dist",
  "installCommand": "npm install"
}
```

## 🚨 Troubleshooting

### Common Issues:

1. **Build Fails**:
   - Check `package.json` syntax
   - Ensure all dependencies are listed

2. **404 Errors**:
   - Verify `vercel.json` routes configuration
   - Check file paths are correct

3. **Slow Loading**:
   - Images should be optimized
   - Check caching headers in `vercel.json`

### Debug Commands:

```bash
# Test locally
vercel dev

# Check deployment logs
vercel logs

# Inspect deployment
vercel inspect
```

## 📈 Analytics & Monitoring

Vercel provides built-in:
- **Web Analytics** (page views, performance)
- **Speed Insights** (Core Web Vitals)
- **Function logs** (if using serverless functions)

Enable in project settings → Analytics

## 🔒 Security Features

- **HTTPS by default**
- **Security headers** configured
- **DDoS protection**
- **Automatic SSL certificates**

## 💰 Pricing

- **Hobby Plan**: Free for personal projects
- **Pro Plan**: $20/month for commercial use
- **Enterprise**: Custom pricing

## 🎯 Next Steps

After deployment:

1. **Test all functionality**
2. **Set up custom domain**
3. **Configure analytics**
4. **Set up monitoring**
5. **Share your live site!**

## 📞 Support

- **Vercel Docs**: [vercel.com/docs](https://vercel.com/docs)
- **Community**: [github.com/vercel/vercel/discussions](https://github.com/vercel/vercel/discussions)
- **Status**: [vercel-status.com](https://vercel-status.com)

---

🎉 **Your AgriScope website is now ready for the world!**
