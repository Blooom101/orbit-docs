# Mintlify Deployment Guide

Your Orbit documentation is now on GitHub and ready to deploy to Mintlify.

## Repository

- **URL**: https://github.com/Blooom101/orbit-docs
- **Branch**: `main`
- **Status**: Pushed and ready

## Deploy to Mintlify (2 minutes)

### Step 1: Sign up / Log in to Mintlify

Go to https://dashboard.mintlify.com and sign up with your GitHub account.

### Step 2: Connect Repository

1. Click **"Create Documentation"** or **"Add Project"**
2. Select **GitHub** as the source
3. Authorize Mintlify to access your GitHub account
4. Find and select `orbit-docs` repository
5. Click **"Install and Continue"**

### Step 3: Configure

Mintlify will auto-detect `mint.json`. Review:
- **Project Name**: "Orbit" (or your preference)
- **Default Subdomain**: Choose custom domain (e.g., `orbit-docs`)
- **Repository**: Confirmed as `Blooom101/orbit-docs`

### Step 4: Deploy

1. Click **"Deploy"**
2. Wait for build to complete (usually < 1 minute)
3. Your docs are live at: `https://[subdomain].mintlify.dev`

## Custom Domain (Optional)

To use your own domain (e.g., `docs.orbitagents.xyz`):

1. In Mintlify dashboard, go to **Settings**
2. Click **"Custom Domain"**
3. Enter your domain
4. Add DNS records (Mintlify provides exact records)
5. Wait for HTTPS certificate to provision (< 5 minutes)

## Auto-Deploy on Push

Once connected, every push to `main` automatically redeploys your docs. No manual steps needed.

## Local Preview (Optional)

To test changes locally before pushing:

```bash
npm install -g @mintlify/cli
cd orbitagents-docs
mintlify dev
```

Opens at http://localhost:3000

## Customize Branding

Edit `mint.json` to:
- Change colors
- Update logo/favicon paths
- Modify footer and social links
- Adjust navigation

Then push to auto-deploy:

```bash
git add mint.json
git commit -m "Update branding"
git push
```

## Next Steps

1. **Deploy now** - Go to https://dashboard.mintlify.com
2. **Customize** - Update colors, logo, domain
3. **Share** - Send docs link to team
4. **Monitor** - Check analytics in Mintlify dashboard
5. **Update** - Add content via git push

## Support

- Mintlify docs: https://mintlify.com/docs
- Contact Mintlify: https://mintlify.com/contact

---

**Documentation Status**: ✅ Complete and deployment-ready  
**Last Updated**: June 28, 2026
