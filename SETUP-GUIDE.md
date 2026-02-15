# Village Organics Website - Complete Setup Guide

## 📦 Files Included

### HTML File
- `village-organics-with-favicon.html` - Complete website with all features

### Favicon Files
- `favicon.ico` - Standard favicon (16x16, 32x32, 48x48, 64x64)
- `favicon-16.png` - 16x16 PNG
- `favicon-32.png` - 32x32 PNG
- `favicon-48.png` - 48x48 PNG
- `favicon-64.png` - 64x64 PNG
- `favicon-128.png` - 128x128 PNG
- `favicon-256.png` - 256x256 PNG (also used for Apple Touch Icon)
- `favicon-512.png` - 512x512 PNG (high resolution)

## 🎨 Favicon Design

The favicon features:
- **Three organic leaves** in various shades of green
- **Seed dots** at the base representing natural farming
- **Circular design** with sage green background
- **Cream/beige center** matching your website's earthy palette
- Professional and instantly recognizable

## 🚀 Quick Setup Instructions

### 1. Upload Files to Your Server
Upload all files to your web server's root directory:
```
your-website.com/
├── index.html (rename village-organics-with-favicon.html to index.html)
├── favicon.ico
├── favicon-16.png
├── favicon-32.png
├── favicon-48.png
├── favicon-64.png
├── favicon-128.png
├── favicon-256.png
└── favicon-512.png
```

### 2. Configure Razorpay Payment Gateway

1. **Sign up at Razorpay:**
   - Go to https://razorpay.com
   - Create a business account
   - Complete KYC verification

2. **Get API Keys:**
   - Login to Razorpay Dashboard
   - Go to Settings → API Keys
   - Generate Test Keys (for testing)
   - Generate Live Keys (for production)

3. **Update HTML File:**
   - Open `village-organics-with-favicon.html`
   - Find line ~1189: `key: 'YOUR_RAZORPAY_KEY_ID'`
   - Replace with your actual Razorpay Key ID
   - Example: `key: 'rzp_live_xxxxxxxxxx'`

4. **Test Payment:**
   - Use test key for testing: `rzp_test_xxxxxxxxxx`
   - Razorpay provides test card numbers
   - Switch to live key when ready for production

### 3. Configure PhonePe QR Code

**Option A: Use UPI ID (Current Setup)**
- Current UPI ID in code: `villageorganics@ybl`
- Update this with your actual UPI ID
- Find line with `villageorganics@ybl` and replace

**Option B: Generate QR Code Image**
1. Go to https://www.phonepe.com/business-solutions/
2. Generate your UPI QR code
3. Download the QR code image
4. Replace the emoji 📱 with your QR image:
```html
<div class="qr-code">
    <img src="phonepe-qr.png" alt="PhonePe QR Code" style="width: 100%; height: 100%;">
</div>
```

### 4. Update WhatsApp Number

Current WhatsApp number: **+91 9986618659**

To change it, search and replace all instances:
- Line ~1156: WhatsApp float button
- Line ~1426: Order function
- Footer section

Replace with your number format: `919876543210` (country code + number, no spaces)

### 5. Test Everything

**Before Going Live:**
✅ Test Razorpay payment with test keys
✅ Click WhatsApp button - should open chat
✅ Test cart add/remove functionality
✅ Check PhonePe QR code displays correctly
✅ Verify favicon appears in browser tab
✅ Test on mobile devices
✅ Check all links work

## 💳 Payment Gateway Fees

### Razorpay
- **Domestic Cards:** 2% + GST
- **International Cards:** 3% + GST
- **UPI:** 2% + GST
- **Net Banking:** 2% + GST
- **Wallets:** 2% + GST
- **No setup fees or annual fees**

### PhonePe/UPI Direct
- **FREE** - No transaction fees
- Customer pays directly to your UPI ID
- Manual confirmation required

## 📱 Mobile Optimization

The website is fully responsive and optimized for:
- ✅ iOS Safari
- ✅ Android Chrome
- ✅ All modern browsers
- ✅ Touch-friendly buttons
- ✅ Optimized font sizes
- ✅ Fast loading

## 🎨 Customization Guide

### Change Colors
Edit the CSS variables in the `<style>` section:
```css
:root {
    --sage-green: #6b8e23;      /* Primary green */
    --forest-green: #2d5016;     /* Dark green */
    --terracotta: #c9653c;       /* Accent color */
    --cream: #faf6f1;            /* Background */
    --earth-dark: #2c1810;       /* Text color */
}
```

### Add More Products
Copy a product card and modify:
```html
<div class="product-card">
    <div class="product-image">🌿</div>
    <div class="product-content">
        <h3 class="product-title">Your Product Name</h3>
        <div class="product-price">₹XXX</div>
        <button onclick="addToCart('Product Name', PRICE, '🌿')">
            Add to Cart
        </button>
    </div>
</div>
```

### Update Contact Information
- **Email:** Search for `info@villageorganics.com` and replace
- **Phone:** Search for `+91 99866186594` and replace
- **Address:** Update in footer section

## 🔒 Security Best Practices

1. **HTTPS Only:** Use SSL certificate (free from Let's Encrypt)
2. **Razorpay Keys:** Never expose secret keys in client-side code
3. **Verify Payments:** Always verify payment status on server-side
4. **Regular Backups:** Backup your website regularly
5. **Update Dependencies:** Keep all libraries updated

## 📊 Analytics Setup (Optional)

### Add Google Analytics
Add before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🐛 Troubleshooting

### Favicon Not Showing
- Clear browser cache (Ctrl + Shift + R)
- Check file paths are correct
- Ensure all favicon files are uploaded
- Wait 24 hours for browser cache to update

### Payment Not Working
- Check Razorpay key is correct (live vs test)
- Verify account is activated
- Check browser console for errors
- Test with Razorpay test cards first

### WhatsApp Not Opening
- Verify phone number format: 919876543210
- No spaces, dashes, or special characters
- Include country code (91 for India)

### Cart Not Working
- Check JavaScript console for errors
- Ensure Font Awesome is loading
- Clear browser cache

## 📞 Support

For Razorpay support: support@razorpay.com
For PhonePe support: https://www.phonepe.com/contact-us/

## ✅ Launch Checklist

Before going live:
- [ ] All favicons uploaded
- [ ] Razorpay LIVE key configured
- [ ] WhatsApp number updated
- [ ] PhonePe UPI ID updated
- [ ] Contact information updated
- [ ] Test all payment methods
- [ ] Test on mobile devices
- [ ] SSL certificate installed
- [ ] Google Analytics added (optional)
- [ ] Privacy Policy added (required for payments)
- [ ] Terms & Conditions added

## 🎉 You're Ready!

Your Village Organics website is now complete with:
✅ Beautiful organic design
✅ Professional favicon
✅ Multiple payment options
✅ WhatsApp integration
✅ Mobile-friendly
✅ Shopping cart
✅ Ready for production

Good luck with your organic products business! 🌾🥥

---
Created with ❤️ for Village Organics
