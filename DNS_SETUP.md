# 🌐 DNS Setup Guide for buildaiwithkartikey.site

## Current Status:
✅ Domain added to Netlify: `buildaiwithkartikey.site`
⏳ DNS propagating (waiting...)
⏳ SSL certificate pending (will auto-generate after DNS)

---

## Step-by-Step DNS Configuration

### Option 1: Use Netlify DNS (Recommended - Easiest)

1. **In Netlify Dashboard:**
   - Go to your site → Domain management
   - Click on `buildaiwithkartikey.site`
   - Click "Options" → "Set up Netlify DNS"
   - You'll see 4 nameservers (like `dns1.p01.nsone.net`)

2. **In Your Domain Provider (Namecheap/GoDaddy/etc.):**
   - Go to Domain settings → Nameservers
   - Change from "Default" to "Custom"
   - Add the 4 nameservers Netlify gave you
   - Save

3. **Wait 5-60 minutes** → DNS will propagate automatically!

---

### Option 2: Manual DNS Records (If you want to keep your domain provider's DNS)

**Add these records in your domain provider's DNS settings:**

```
Record 1:
Type: A
Name: @ (or leave blank)
Value: 75.2.60.5
TTL: 3600 (or Auto)

Record 2:
Type: CNAME
Name: www
Value: glittering-stardust-91bb6e.netlify.app
TTL: 3600 (or Auto)
```

**Where to add:**
- Namecheap: Domain List → Manage → Advanced DNS
- GoDaddy: DNS Management → Add Record
- Cloudflare: DNS → Add record
- Google Domains: DNS → Custom records

---

## Common Domain Providers:

### Namecheap:
1. Login → Domain List
2. Click "Manage" next to your domain
3. Go to "Advanced DNS" tab
4. Add records as shown above

### GoDaddy:
1. Login → My Products
2. Click "DNS" next to your domain
3. Click "Add" to add new records
4. Add A and CNAME records

### Cloudflare:
1. Select your domain
2. Go to DNS → Records
3. Add A and CNAME records

---

## After DNS Setup:

1. **Wait 5-60 minutes** for DNS propagation
2. Check status in Netlify → Domain management
3. Status will change from "Propagating..." to "Active"
4. SSL certificate will auto-generate (HTTPS will work)
5. Your site will be live at: `https://buildaiwithkartikey.site`

---

## Troubleshooting:

**If DNS not working after 1 hour:**
- Double-check nameservers/DNS records
- Use DNS checker: https://dnschecker.org
- Check if domain is unlocked (not locked for transfer)

**If SSL certificate still failing:**
- Wait for DNS to fully propagate (can take up to 24 hours)
- Make sure domain is not behind Cloudflare proxy (if using Cloudflare)
- Contact Netlify support if issue persists

---

## Quick Test:

Once DNS propagates, test your site:
- `https://buildaiwithkartikey.site` ✅
- `https://www.buildaiwithkartikey.site` ✅ (auto-redirects)

**Your portfolio is live! 🚀**
