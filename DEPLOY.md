# GitHub Pages Deployment Instructions

This folder contains the production-ready static files for your RunAtom website.

## Quick Start

### Option 1: Deploy to GitHub Pages (Recommended)

1. **Create a new GitHub repository** (e.g., `runatom-website`)

2. **Upload these files to your repository:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: RunAtom website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/runatom-website.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repository Settings
   - Navigate to "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Select branch: `main` and folder: `/ (root)`
   - Click "Save"

4. **Your site will be live at:**
   `https://YOUR_USERNAME.github.io/runatom-website/`

### Option 2: Custom Domain on GitHub Pages

If you want to use `runatom.com`:

1. Follow steps 1-3 above
2. In GitHub Pages settings, add your custom domain: `runatom.com`
3. Create a `CNAME` file in the root with content: `runatom.com`
4. Configure your DNS:
   - Add an A record pointing to GitHub's IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Or add a CNAME record pointing to: `YOUR_USERNAME.github.io`

## Before Deploying

### Update Placeholder URLs

Edit `index.html` and search for these placeholders:

1. **Contact Form** - Replace `https://forms.gle/your-form-id` with your actual form URL
2. **Upwork Profile** - Replace `#` in Upwork link with your profile URL
3. **LinkedIn Profile** - Replace `#` in LinkedIn link with your profile URL

You can edit the `index.html` file directly, or make changes in the source code and rebuild.

## Files Included

- `index.html` - Main HTML file
- `assets/` - CSS, JavaScript, and other assets
- All files are minified and optimized for production

## Alternative Hosting Options

These static files can also be deployed to:
- **Netlify**: Drag and drop this folder to netlify.com/drop
- **Vercel**: Use `vercel --prod` in this directory
- **Cloudflare Pages**: Connect your GitHub repo or upload directly
- **Any static hosting**: Upload via FTP/SFTP to your web server

## Troubleshooting

**Issue**: Links don't work after deployment
**Solution**: Make sure all internal links use relative paths (they already do in this build)

**Issue**: Custom domain not working
**Solution**: DNS changes can take 24-48 hours to propagate. Be patient!

**Issue**: Need to update content
**Solution**: Either edit `index.html` directly, or modify the source files in the Manus project and rebuild

## Support

For questions about the website code or customization, refer to `CUSTOMIZATION.md` in the original project.
