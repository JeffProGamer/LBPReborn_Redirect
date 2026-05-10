# LBP Reborn - Lighthouse GitHub Pages

A GitHub Pages site for your local Lighthouse server with custom domain support.

## Setup Instructions

### 1. Create a GitHub Repository
- Create a new repo named `yourusername.github.io` or any name
- Clone it to your computer

### 2. Add These Files

**CNAME file** (replace with your domain):
```
your-domain.com
```

**index.html** - Already provided with landing page

### 3. Set Up Custom Domain

**Option A: Using your own domain registrar**
1. Add an `A` record pointing to your server IP: `192.168.100.6`
2. Create a `CNAME` file in the repo root with just your domain name

**Option B: Using GitHub's domain**
1. Skip the CNAME file
2. Your site will be at `yourusername.github.io`

### 4. Push to GitHub
```bash
git add .
git commit -m "Add Lighthouse landing page"
git push origin main
```

### 5. Enable GitHub Pages
1. Go to repository Settings → Pages
2. Set source to `main` branch
3. Add custom domain (if using your own domain)

### 6. Update DNS (if using custom domain)
- Point your domain to GitHub Pages or your Lighthouse server
- Update dnsmasq to map the domain locally

## Example Domain Setup

If your domain is `get.lbpreborn.local`:

**dnsmasq.conf:**
```
address=/get.lbpreborn.local/192.168.100.6
```

**CNAME file:**
```
get.lbpreborn.local
```

## What's Your Domain?

Let me know your domain name and I'll update the files accordingly!
