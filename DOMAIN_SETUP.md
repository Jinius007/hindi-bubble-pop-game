# 🌐 Domain Setup Guide - Consistent Vercel URL

## 🎯 **Problem**: Vercel URLs Change Every Deployment
By default, Vercel creates URLs like:
- `project-name-git-main-username.vercel.app`
- `project-name-abc123.vercel.app`

These change with each deployment!

## ✅ **Solutions**

### **Option 1: Custom Domain (Best)**
Get a permanent URL like `hindi-games.vercel.app` or `yourdomain.com`

#### **Step 1: Set Up in Vercel Dashboard**
1. Go to your Vercel project dashboard
2. Click **"Settings"** tab
3. Click **"Domains"** section
4. Add your custom domain

#### **Step 2: Choose Domain Type**

**A) Vercel Subdomain (Free)**
- Format: `your-project-name.vercel.app`
- Example: `hindi-games.vercel.app`
- **Pros**: Free, easy setup
- **Cons**: Still has `.vercel.app` suffix

**B) Custom Domain (Paid)**
- Format: `yourdomain.com`
- Example: `hindigames.com`
- **Pros**: Professional, memorable
- **Cons**: Requires domain purchase (~$10-15/year)

#### **Step 3: Configure DNS**
For custom domains, you'll need to update DNS settings:
```
Type: CNAME
Name: @ or www
Value: cname.vercel-dns.com
```

### **Option 2: Production Branch (Free)**
Make your main branch the production branch so it always deploys to the same URL.

#### **Step 1: Configure in Vercel**
1. Go to project settings
2. Under **"Git"** section
3. Set **"Production Branch"** to `main`
4. This ensures `main` branch always deploys to the same URL

### **Option 3: Vercel CLI Alias (Free)**
Use Vercel CLI to create a permanent alias.

#### **Step 1: Install Vercel CLI**
```bash
npm i -g vercel
```

#### **Step 2: Login and Link**
```bash
vercel login
vercel link
```

#### **Step 3: Deploy with Alias**
```bash
vercel --prod --alias your-project-name.vercel.app
```

## 🚀 **Recommended Setup**

### **For Free Option:**
1. **Use Vercel Subdomain**: `hindi-games.vercel.app`
2. **Set Production Branch**: `main`
3. **Always deploy from main branch**

### **For Professional Option:**
1. **Buy a domain**: `hindigames.com` or similar
2. **Configure DNS** with Vercel
3. **Set up SSL** (automatic with Vercel)

## 📋 **Step-by-Step Instructions**

### **Free Setup (Vercel Subdomain)**
1. Go to Vercel Dashboard → Your Project → Settings
2. Click "Domains"
3. Add domain: `hindi-games.vercel.app`
4. Go to "Git" section
5. Set "Production Branch" to `main`
6. Deploy from main branch only

### **Custom Domain Setup**
1. **Buy domain** from Namecheap, GoDaddy, etc.
2. **Add domain** in Vercel dashboard
3. **Update DNS** records as instructed
4. **Wait for propagation** (up to 48 hours)
5. **SSL certificate** will be auto-generated

## 🔧 **Deployment Commands**

### **Always Deploy to Same URL:**
```bash
# Deploy to production (main branch)
git push origin main

# Or with Vercel CLI
vercel --prod
```

### **Check Current URLs:**
```bash
# List all deployments
vercel ls

# Get current production URL
vercel inspect
```

## 📱 **Mobile-Friendly URLs**

Your games will be accessible at:
- **Main site**: `yourdomain.com` or `hindi-games.vercel.app`
- **Individual games**: 
  - `yourdomain.com/muhawra-mahal`
  - `yourdomain.com/bilingual-train`
  - etc.

## 🎮 **Sharing Your Games**

Once you have a consistent URL, you can share:
- **Main site**: `https://hindi-games.vercel.app`
- **Direct game links**: `https://hindi-games.vercel.app/muhawra-mahal.html`

## 🔄 **Automatic Deployments**

Set up GitHub integration so every push to `main` automatically deploys to your consistent URL:

1. **Connect GitHub** in Vercel
2. **Set production branch** to `main`
3. **Auto-deploy** on every push

## 📊 **Analytics with Consistent URL**

With a consistent URL, you can:
- **Track long-term trends** in Google Analytics
- **Build SEO** for your Hindi learning games
- **Share links** that never break
- **Monitor performance** over time

## 🎯 **Next Steps**

1. **Choose your domain option** (free subdomain or custom domain)
2. **Set up in Vercel dashboard**
3. **Deploy from main branch only**
4. **Test your consistent URL**
5. **Share with users!**

---

**💡 Tip**: Start with the free Vercel subdomain (`hindi-games.vercel.app`) and upgrade to a custom domain later if needed!
