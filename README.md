
# Kalyan Ayurveda Patanjali Store - Deployment Guide

This guide fixes the "404 Not Found" and "Build Failed" errors.

## Step 1: Update Your Repository
Ensure **ALL** files are uploaded to GitHub, especially these three critical ones:
1. `package.json` (The build instructions)
2. `tsconfig.json` (The TypeScript rules)
3. `vite.config.ts` (The website compiler)

## Step 2: Deploying to Netlify (Recommended)
If you are using Netlify:
1. Connect your GitHub repository.
2. **Build Settings**:
   - Build command: `npm run build`
   - Publish directory: `dist`
3. **Environment Variables**:
   - Go to **Site Configuration** > **Environment variables**.
   - Add `API_KEY` and paste your Gemini API Key.
4. **Trigger Deploy**: Your site should now build successfully!

## Step 3: Deploying to Vercel
If you are using Vercel:
1. Connect your GitHub repository.
2. **Framework Preset**: Select **Vite**.
3. **Environment Variables**: Add `API_KEY`.
4. Click **Deploy**.

## Accessing the Admin Panel
Once live at `yoursite.com`:
- Go to: `yoursite.com/?mode=admin`
- Default PIN: `2025`

## Common Fixes
- **Build Fails?** Ensure you have committed the new `tsconfig.json` file.
- **404 Error on Refresh?** Ensure `vercel.json` (for Vercel) or a `_redirects` file (for Netlify) is in your project.
