# Netlify Build Fix - Step by Step Instructions

## Problem
Netlify is trying to run "bun run build" but the build script is missing or not found.

## Solution Applied
1. ✅ Created `package.json` with a build script
2. ✅ Updated `netlify.toml` to use `npm run build` instead of bun

## Manual Netlify UI Settings (If Still Having Issues)

### Step 1: Access Build Settings
1. Go to https://app.netlify.com
2. Select your site
3. Go to **Site settings** → **Build & deploy** → **Build settings**
4. Click **"Edit settings"**

### Step 2: Configure Build Settings
Set these exact values:

```
Base directory: (leave EMPTY)
Build command: npm run build
Publish directory: .
```

**OR** if you want to skip the build entirely:

```
Base directory: (leave EMPTY)
Build command: (leave COMPLETELY EMPTY)
Publish directory: .
```

### Step 3: Save and Redeploy
1. Click **"Save"**
2. Go to **Deploys** tab
3. Click **"Trigger deploy"** → **"Deploy site"**

## Alternative: Clear Build Command Completely

If you want Netlify to skip the build step entirely:

1. In Netlify UI: **Build command** → Leave **completely empty**
2. **Publish directory**: Set to `.` (period/dot)
3. This tells Netlify: "No build needed, just publish the files as-is"

## Verify Files Are Committed

Make sure these files are in your GitHub repository:
- ✅ `index.html` (in root)
- ✅ `package.json` (in root)
- ✅ `netlify.toml` (in root)

Check: https://github.com/Jas21j/SalesmanSolutions.net

## If Build Still Fails

### Get Full Error Log
1. In Netlify dashboard, go to **Deploys** tab
2. Click on the failed deployment
3. Click **"Deploy log"**
4. Click **"Download deploy log"** or **"Show more"**
5. Copy the **complete error message** (not just one line)

### Common Issues & Fixes

**Issue**: "Script not found 'build'"
- **Fix**: Ensure `package.json` is committed and has the build script

**Issue**: "Cannot find module"
- **Fix**: This shouldn't happen for static HTML, but if it does, check that all files are committed

**Issue**: "Publish directory not found"
- **Fix**: Set publish directory to `.` (period) in Netlify UI

**Issue**: Netlify using wrong package manager (bun instead of npm)
- **Fix**: Explicitly set build command to `npm run build` in netlify.toml

## Current Configuration

### package.json
```json
{
  "scripts": {
    "build": "echo 'No build required - static HTML site'"
  }
}
```

### netlify.toml
```toml
[build]
  command = "npm run build"
  publish = "."
```

This configuration:
- ✅ Uses npm (not bun)
- ✅ Has a valid build script
- ✅ Publishes from root directory
- ✅ Works locally (tested)

## Next Steps

1. **Wait for auto-deploy**: Netlify should automatically redeploy after the push
2. **Or trigger manually**: Go to Deploys → Trigger deploy
3. **Check logs**: If it still fails, get the full deploy log and share it

The configuration is now correct. If issues persist, the full deploy log will show the exact error.

