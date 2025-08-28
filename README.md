# TechFix Pro - Website Portofolio Servis Handphone & Laptop

Website portofolio modern dan responsif untuk usaha servis handphone dan laptop yang dibuat dengan HTML5, Bootstrap 5, dan JavaScript.

## 🚀 Fitur Utama

### ✨ Desain & UI/UX
- **Desain Modern**: Menggunakan Bootstrap 5 dengan komponen yang elegan
- **Responsif**: Optimal di semua perangkat (desktop, tablet, mobile)
- **Animasi Interaktif**: AOS (Animate On Scroll) untuk efek visual yang menarik
- **Gradient & Shadow**: Kombinasi warna yang bersih dan profesional
- **Hover Effects**: Efek interaktif pada card, button, dan elemen lainnya

### 📱 Navigasi & Struktur
- **Header Fixed**: Navigasi yang tetap di atas saat scroll
- **Smooth Scrolling**: Transisi halus antar section
- **Active Navigation**: Highlight menu yang sedang aktif
- **Mobile Menu**: Toggle menu untuk perangkat mobile

### 🛠️ Section Website
1. **Hero Section**: Headline menarik dengan CTA buttons
2. **Layanan**: 6 jenis layanan dalam card yang informatif
3. **Portofolio**: Showcase hasil pekerjaan dengan ikon
4. **Testimoni**: Carousel testimoni pelanggan
5. **Kontak**: Form kontak dan informasi lengkap
6. **Footer**: Informasi tambahan dan social media links

### 💻 Teknologi yang Digunakan
- **HTML5**: Semantic markup yang bersih
- **Bootstrap 5**: Framework CSS untuk layout responsif
- **Bootstrap Icons**: Ikon yang konsisten dan modern
- **AOS Library**: Animasi scroll yang smooth
- **Vanilla JavaScript**: Interaktivitas tanpa framework
- **CSS3**: Custom styling dengan variabel CSS

## 📁 Struktur File

```
techfix-pro-portfolio/
├── index.html          # File HTML utama
├── style.css           # Custom CSS styling
├── script.js           # JavaScript functionality
└── README.md           # Dokumentasi
```

## 🎨 Komponen Website

### Header/Navigation
- Logo dengan ikon tools
- Menu navigasi (Home, Layanan, Portofolio, Testimoni, Kontak)
- Responsive hamburger menu untuk mobile
- Background blur effect saat scroll

### Hero Section
- Gradient background yang menarik
- Headline dengan typography yang bold
- Deskripsi singkat tentang layanan
- CTA buttons (Lihat Layanan, Hubungi Kami)
- Animasi floating icons

### Layanan Section
- 6 card layanan dengan ikon yang berbeda:
  - Servis Handphone
  - Servis Laptop
  - Instalasi Software
  - Data Recovery
  - Networking
  - Maintenance
- Hover effects dengan transform dan shadow
- Detail layanan dalam list format

### Portofolio Section
- Grid layout dengan 6 item portofolio
- Ikon representatif untuk setiap jenis pekerjaan
- Hover effects dengan scale dan color change
- Animasi zoom-in saat scroll

### Testimoni Section
- Bootstrap carousel dengan 3 testimoni
- Avatar placeholder dengan ikon
- Quote marks styling
- Auto-play dengan interval 5 detik
- Navigation controls

### Kontak Section
- Split layout: informasi kontak + form
- Contact icons dengan gradient background
- Social media links dengan hover effects
- Form validation (email, phone, required fields)
- Success notification system

### Footer
- 3 kolom informasi (tentang, layanan, kontak)
- Social media links
- Copyright information
- Gradient background

## 🎯 Fitur JavaScript

### Interaktivitas
- **Smooth Scrolling**: Navigasi halus antar section
- **Form Validation**: Validasi real-time untuk form kontak
- **Notification System**: Alert untuk feedback user
- **Back to Top**: Button untuk kembali ke atas
- **Mobile Menu**: Toggle untuk navigasi mobile

### Animasi & Effects
- **AOS Integration**: Scroll-based animations
- **Hover Effects**: Transform dan shadow effects
- **Loading States**: Button loading animation
- **Parallax Effect**: Hero section parallax
- **Typing Effect**: Optional typing animation untuk hero title

### Performance
- **Debounced Scroll**: Optimized scroll handling
- **Lazy Loading**: Image lazy loading support
- **Intersection Observer**: Efficient animation triggers
- **Service Worker**: PWA support (optional)

## 🚀 Cara Penggunaan

### 1. Setup Lokal
```bash
# Clone atau download file
# Buka folder project
cd techfix-pro-portfolio

# Buka file index.html di browser
# Atau gunakan live server
```

### 2. Customization

#### Mengubah Informasi Kontak
Edit bagian kontak di `index.html`:
```html
<!-- Ganti informasi sesuai kebutuhan -->
<p class="text-muted mb-0">+62 812-3456-7890</p>
<p class="text-muted mb-0">info@techfixpro.com</p>
<p class="text-muted mb-0">Jl. Teknologi No. 123, Jakarta Selatan</p>
```

#### Mengubah Social Media Links
Edit di `script.js`:
```javascript
case 'bi-facebook':
    url = 'https://facebook.com/yourpage';
    break;
case 'bi-instagram':
    url = 'https://instagram.com/yourpage';
    break;
```

#### Mengubah Warna Theme
Edit CSS variables di `style.css`:
```css
:root {
    --primary-color: #0d6efd;    /* Warna utama */
    --secondary-color: #6c757d;  /* Warna sekunder */
    /* ... */
}
```

### 3. Deployment
- Upload semua file ke web hosting
- Pastikan semua CDN links berfungsi
- Test responsiveness di berbagai device

## 📱 Responsive Breakpoints

- **Desktop**: > 992px
- **Tablet**: 768px - 991px
- **Mobile**: < 767px

## 🎨 Color Scheme

- **Primary**: #0d6efd (Bootstrap Blue)
- **Secondary**: #6c757d (Gray)
- **Success**: #198754 (Green)
- **Dark**: #212529 (Dark Gray)
- **Light**: #f8f9fa (Light Gray)

## 🔧 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📈 Performance Features

- **Optimized Images**: Lazy loading support
- **Minified CSS/JS**: Ready for production
- **CDN Resources**: Fast loading external libraries
- **Debounced Events**: Smooth performance
- **Intersection Observer**: Efficient animations

## 🛠️ Customization Guide

### Menambah Layanan Baru
1. Copy template card di section layanan
2. Ganti ikon, judul, dan deskripsi
3. Update form dropdown di section kontak

### Menambah Testimoni
1. Copy carousel item template
2. Ganti nama, testimoni, dan profesi
3. Update carousel indicators jika perlu

### Mengubah Animasi
1. Edit AOS attributes di HTML
2. Customize CSS animations
3. Modify JavaScript timing

## 📞 Support

Untuk pertanyaan atau bantuan:
- Email: info@techfixpro.com
- WhatsApp: +62 812-3456-7890

## 📄 License

Website ini dibuat untuk tujuan portofolio dan dapat digunakan secara bebas untuk keperluan komersial.

---

**TechFix Pro** - Solusi lengkap untuk perbaikan gadget Anda! 🛠️📱💻
