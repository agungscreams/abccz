# Deployment Guide - TechFix Pro Portfolio Website

Panduan lengkap untuk deploy website portofolio TechFix Pro ke berbagai platform hosting.

## 🚀 Platform Deployment

### 1. GitHub Pages (Gratis)

#### Setup Repository
```bash
# Buat repository baru di GitHub
# Clone repository
git clone https://github.com/yourusername/techfix-pro-portfolio.git
cd techfix-pro-portfolio

# Upload semua file
git add .
git commit -m "Initial commit: TechFix Pro Portfolio Website"
git push origin main
```

#### Enable GitHub Pages
1. Buka repository di GitHub
2. Klik **Settings** → **Pages**
3. Pilih **Source**: Deploy from a branch
4. Pilih **Branch**: main
5. Klik **Save**
6. Website akan tersedia di: `https://yourusername.github.io/techfix-pro-portfolio`

### 2. Netlify (Gratis)

#### Drag & Drop Method
1. Buka [netlify.com](https://netlify.com)
2. Sign up/Login
3. Drag folder project ke area deploy
4. Website akan otomatis ter-deploy

#### Git Integration
1. Connect repository GitHub/GitLab
2. Pilih repository
3. Build settings:
   - Build command: (kosongkan)
   - Publish directory: (kosongkan)
4. Klik **Deploy site**

### 3. Vercel (Gratis)

#### CLI Deployment
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Follow prompts
# Website akan tersedia di: https://your-project.vercel.app
```

#### Git Integration
1. Buka [vercel.com](https://vercel.com)
2. Import repository dari GitHub
3. Configure project settings
4. Deploy otomatis

### 4. Shared Hosting (cPanel)

#### Upload via File Manager
1. Login ke cPanel
2. Buka **File Manager**
3. Navigasi ke `public_html`
4. Upload semua file project
5. Website tersedia di domain Anda

#### Upload via FTP
```bash
# Gunakan FTP client seperti FileZilla
Host: your-domain.com
Username: your-username
Password: your-password
Port: 21

# Upload semua file ke public_html/
```

### 5. VPS/Dedicated Server

#### Nginx Configuration
```nginx
server {
    listen 80;
    server_name techfixpro.com www.techfixpro.com;
    root /var/www/techfix-pro-portfolio;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }

    # Enable gzip compression
    gzip on;
    gzip_types text/css application/javascript text/html;

    # Cache static files
    location ~* \.(css|js|png|jpg|jpeg|gif|ico|svg)$ {
        expires 1y;
        add_header Cache-Control "public, immutable";
    }
}
```

#### Apache Configuration
```apache
<VirtualHost *:80>
    ServerName techfixpro.com
    ServerAlias www.techfixpro.com
    DocumentRoot /var/www/techfix-pro-portfolio
    
    <Directory /var/www/techfix-pro-portfolio>
        AllowOverride All
        Require all granted
    </Directory>
    
    # Enable compression
    <IfModule mod_deflate.c>
        AddOutputFilterByType DEFLATE text/html text/css application/javascript
    </IfModule>
    
    # Cache static files
    <IfModule mod_expires.c>
        ExpiresActive On
        ExpiresByType text/css "access plus 1 year"
        ExpiresByType application/javascript "access plus 1 year"
        ExpiresByType image/png "access plus 1 year"
        ExpiresByType image/jpg "access plus 1 year"
        ExpiresByType image/jpeg "access plus 1 year"
        ExpiresByType image/gif "access plus 1 year"
        ExpiresByType image/ico "access plus 1 year"
        ExpiresByType image/svg+xml "access plus 1 year"
    </IfModule>
</VirtualHost>
```

## 🔧 Pre-Deployment Checklist

### 1. Update URLs
```html
<!-- Ganti semua URL di index.html -->
<meta property="og:url" content="https://yourdomain.com">
<meta property="og:image" content="https://yourdomain.com/og-image.jpg">
<link rel="canonical" href="https://yourdomain.com">
```

### 2. Update Contact Information
```html
<!-- Update informasi kontak -->
<p class="text-muted mb-0">+62 812-3456-7890</p>
<p class="text-muted mb-0">info@yourdomain.com</p>
<p class="text-muted mb-0">Jl. Your Address, Your City</p>
```

### 3. Update Social Media Links
```javascript
// Update di script.js
case 'bi-facebook':
    url = 'https://facebook.com/yourpage';
    break;
case 'bi-instagram':
    url = 'https://instagram.com/yourpage';
    break;
```

### 4. Update Sitemap
```xml
<!-- Update sitemap.xml -->
<loc>https://yourdomain.com/</loc>
<loc>https://yourdomain.com/#layanan</loc>
```

## 📱 PWA Configuration

### 1. Update Manifest
```json
{
  "name": "Your Business Name",
  "short_name": "Your Brand",
  "start_url": "/",
  "scope": "/"
}
```

### 2. Generate Icons
```bash
# Gunakan tools online untuk generate icons
# https://realfavicongenerator.net/
# https://www.pwabuilder.com/imageGenerator
```

### 3. Test PWA
1. Buka Chrome DevTools
2. Tab **Application** → **Manifest**
3. Tab **Application** → **Service Workers**
4. Test install prompt

## 🔍 SEO Optimization

### 1. Google Search Console
1. Daftar website di [Google Search Console](https://search.google.com/search-console)
2. Verify ownership
3. Submit sitemap.xml
4. Monitor performance

### 2. Google Analytics
```html
<!-- Tambahkan di <head> -->
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### 3. Meta Tags
```html
<!-- Pastikan semua meta tags sudah benar -->
<meta name="description" content="Your business description">
<meta name="keywords" content="your, keywords, here">
```

## 🚀 Performance Optimization

### 1. Enable Compression
```nginx
# Nginx
gzip on;
gzip_types text/css application/javascript text/html;
```

### 2. Set Cache Headers
```nginx
# Cache static files
location ~* \.(css|js|png|jpg|jpeg|gif|ico|svg)$ {
    expires 1y;
    add_header Cache-Control "public, immutable";
}
```

### 3. Optimize Images
```bash
# Compress images sebelum upload
# Gunakan tools seperti TinyPNG, ImageOptim
```

## 🔒 Security

### 1. HTTPS Setup
```bash
# Let's Encrypt (gratis)
sudo certbot --nginx -d yourdomain.com -d www.yourdomain.com
```

### 2. Security Headers
```nginx
# Nginx security headers
add_header X-Frame-Options "SAMEORIGIN" always;
add_header X-XSS-Protection "1; mode=block" always;
add_header X-Content-Type-Options "nosniff" always;
add_header Referrer-Policy "no-referrer-when-downgrade" always;
add_header Content-Security-Policy "default-src 'self' http: https: data: blob: 'unsafe-inline'" always;
```

## 📊 Monitoring

### 1. Uptime Monitoring
- [UptimeRobot](https://uptimerobot.com) - Gratis
- [Pingdom](https://pingdom.com) - Berbayar

### 2. Performance Monitoring
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)
- [WebPageTest](https://www.webpagetest.org/)

## 🆘 Troubleshooting

### Common Issues

#### 1. 404 Errors
```bash
# Pastikan file index.html ada di root directory
# Check file permissions (644 untuk files, 755 untuk directories)
```

#### 2. CSS/JS Not Loading
```bash
# Check file paths
# Verify file permissions
# Check browser console for errors
```

#### 3. PWA Not Working
```bash
# Verify manifest.json syntax
# Check service worker registration
# Test in incognito mode
```

#### 4. SEO Issues
```bash
# Submit sitemap to search engines
# Check robots.txt
# Verify meta tags
```

## 📞 Support

Untuk bantuan deployment:
- Email: support@yourdomain.com
- WhatsApp: +62 812-3456-7890
- Documentation: [GitHub Wiki](https://github.com/yourusername/techfix-pro-portfolio/wiki)

---

**TechFix Pro** - Ready to deploy! 🚀
