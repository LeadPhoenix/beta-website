# LeadPhoenix Landing Page

## Deploy to Vercel (Step by Step)

### 1. Push to GitHub
```bash
# Create a new repo on github.com (private recommended)
# Then in your terminal:
cd leadphoenix-site
git init
git add .
git commit -m "Initial landing page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/leadphoenix-site.git
git push -u origin main
```

### 2. Connect to Vercel
1. Go to [vercel.com](https://vercel.com) and sign up with your GitHub account
2. Click "Add New Project"
3. Import your `leadphoenix-site` repository
4. Vercel auto-detects Vite — just click "Deploy"
5. Wait ~60 seconds. Your site is live at `leadphoenix-site.vercel.app`

### 3. Connect Your Domain
1. In Vercel dashboard → your project → Settings → Domains
2. Add `leadphoenix.ai`
3. Vercel will give you DNS records to add
4. In Namecheap → Domain List → leadphoenix.ai → Advanced DNS:
   - Option A (recommended): Change nameservers to Vercel's nameservers
   - Option B: Add a CNAME record pointing to `cname.vercel-dns.com`
5. Wait for DNS propagation (usually 5-30 minutes)
6. Vercel auto-provisions SSL. Site is live at `leadphoenix.ai`

### 4. Future Updates
```bash
# Make changes, then:
git add .
git commit -m "Update landing page"
git push
# Vercel auto-deploys in ~30 seconds
```

## Local Development
```bash
npm install
npm run dev
# Opens at http://localhost:5173
```

## Build for Production
```bash
npm run build
# Output in /dist folder
```
