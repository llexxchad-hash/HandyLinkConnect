# HandyLink - Web Application

This repository contains the **Expo web build** of the HandyLink mobile app, ready for deployment to your custom domain.

## 📦 What's Inside

- **`deploy` branch**: Contains the built web app (HTML, CSS, JS) ready for deployment
- **`master` branch**: Documentation and setup instructions

## 🚀 Quick Start - Connect Your Domain

### Option 1: Deploy to Netlify (Recommended - Free & Easy)

1. Go to [netlify.com](https://netlify.com) and sign up
2. Click **"New site from Git"** → Select this repository
3. Set build command: leave empty (we have pre-built files)
4. Set publish directory: `dist/`
5. Connect your domain:
   - In Netlify: Domain settings → Add custom domain
   - In your domain registrar: Point nameservers to Netlify's or set CNAME records
   - Netlify provides free SSL certificate automatically

### Option 2: Deploy to Vercel (Free & Fast)

1. Go to [vercel.com](https://vercel.com) and sign up
2. Import this GitHub repository
3. Set root directory: `dist`
4. Deploy and connect your domain through Vercel dashboard

### Option 3: Traditional Hosting (Any Web Host)

1. Download the `dist/` folder contents
2. Upload via FTP/SFTP to your web host
3. Point your domain to the host
4. Ensure your web server serves `index.html` for all routes (SPA)

### Option 4: GitHub Pages

1. Settings → Pages → Source: Deploy from branch
2. Select `deploy` branch and `root` folder
3. Your site will be at: `https://username.github.io/HandyLinkConnect`
4. For custom domain: Add CNAME file and update DNS

## 📝 DNS Configuration

To connect your purchased domain:

**If using Netlify/Vercel:**
- They'll provide DNS records or nameservers
- Update these at your domain registrar

**If using traditional hosting:**
- Update A records to your host's IP address
- Or update CNAME record as provided by your host

## 🔄 Updating the App

When you want to update the web app:

1. Build locally: `expo export --platform web`
2. Copy new `dist/` folder to `deploy` branch
3. Commit and push: 
   ```bash
   git add dist/
   git commit -m "Update: web app build"
   git push origin deploy
   ```
4. Your deployment platform will auto-rebuild

## 📋 Available Branches

- **`deploy`** - Production-ready web app build (push here to auto-deploy)
- **`master`** - This documentation

## ⚙️ Environment Configuration

The web app uses environment variables from `.env.local` when building. Make sure sensitive credentials are:
- Never committed to Git
- Set via your deployment platform's environment settings

## 🆘 Troubleshooting

**App shows 404 page?**
- Ensure your server routes all requests to `index.html` (Single Page App)
- Netlify/Vercel handle this automatically

**Styles or images not loading?**
- Check that your domain is properly configured
- Verify CORS settings if APIs are remote
- Check browser console for error messages

**Custom domain not working?**
- DNS changes take 5-48 hours to propagate
- Verify DNS records are correctly set
- Test with: `nslookup yourdomain.com`

## 📞 Support

For issues with the app itself, check the main project repository.
For deployment questions, refer to your platform's documentation:
- [Netlify Docs](https://docs.netlify.com/)
- [Vercel Docs](https://vercel.com/docs)
- Your hosting provider's documentation

---

**Ready to go live!** 🎉
