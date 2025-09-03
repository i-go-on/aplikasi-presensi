# 🎯 Aplikasi Presensi QR Code - Dashboard Modern

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/i-go-on/presensi-qr)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=Firebase&logoColor=white)](https://firebase.google.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

> **Sistem presensi modern berbasis QR Code dengan UI yang elegan dan fitur yang lengkap**

## ✨ **Fitur Utama**

### 🎨 **UI/UX Modern**
- **Glassmorphism Design** - Efek transparansi dengan backdrop-filter blur
- **Gradient Backgrounds** - Warna-warna yang menarik dan modern
- **Responsive Design** - Optimized untuk semua device
- **Smooth Animations** - Transisi dan hover effects yang halus
- **Dark/Light Theme** - Tema yang dapat disesuaikan

### 🔐 **Sistem Keamanan**
- **Google Authentication** - Login dengan akun Google yang aman
- **Real-time Database** - Data tersimpan secara real-time di Firebase
- **Geolocation Tracking** - Pencatatan lokasi presensi (opsional)
- **Session Management** - Kontrol sesi presensi yang fleksibel

### 📱 **Fitur Presensi**
- **QR Code Generation** - Generate QR code unik untuk setiap sesi
- **Auto-scan Detection** - Presensi otomatis saat scan QR
- **Attendance History** - Riwayat presensi lengkap
- **Export Data** - Ekspor data ke format CSV
- **Real-time Updates** - Update data secara real-time

## 🚀 **Demo & Screenshots**

### **Admin Dashboard**
![Admin Dashboard](https://via.placeholder.com/800x400/667eea/ffffff?text=Admin+Dashboard+Modern)

### **Peserta Interface**
![Peserta Interface](https://via.placeholder.com/800x400/764ba2/ffffff?text=Peserta+Interface+Modern)

## 🛠️ **Teknologi yang Digunakan**

| Komponen | Teknologi | Versi |
|----------|-----------|-------|
| **Frontend** | HTML5, CSS3, JavaScript (ES6+) | Latest |
| **Styling** | Tailwind CSS | 3.x |
| **Icons** | Font Awesome | 6.4.0 |
| **QR Code** | qrcode.js | 1.5.1 |
| **QR Scanner** | HTML5-QRCode | Latest |
| **Backend** | Firebase | 11.6.1 |
| **Database** | Firestore | Real-time |
| **Authentication** | Firebase Auth | Google Sign-in |

## 📋 **Persyaratan Sistem**

### **Browser Support**
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### **Device Support**
- ✅ Desktop/Laptop
- ✅ Tablet
- ✅ Mobile Phone
- ✅ Progressive Web App (PWA) Ready

### **Requirements**
- **HTTPS Connection** (untuk fitur kamera)
- **Camera Permission** (untuk scan QR)
- **Location Permission** (opsional, untuk tracking)
- **Modern Browser** dengan ES6+ support

## 🚀 **Cara Instalasi & Penggunaan**

### **1. Clone Repository**
```bash
git clone https://github.com/i-go-on/presensi-qr.git
cd presensi-qr
```

### **2. Setup Firebase**
1. Buat project di [Firebase Console](https://console.firebase.google.com/)
2. Enable Authentication dengan Google Sign-in
3. Buat Firestore Database
4. Update konfigurasi di file JavaScript

### **3. Deploy ke Web Server**
- Upload file ke hosting service (Netlify, Vercel, dll)
- Atau gunakan Firebase Hosting
- Pastikan menggunakan HTTPS

### **4. Akses Aplikasi**
- **Admin**: Buka `admin.html`
- **Peserta**: Buka `index.html`

## 📱 **Cara Penggunaan**

### **Untuk Admin**
1. **Login** dengan akun Google
2. **Buat Sesi** baru dengan nama kegiatan
3. **Tampilkan QR Code** kepada peserta
4. **Monitor Kehadiran** secara real-time
5. **Export Data** ke CSV jika diperlukan
6. **Tutup Sesi** setelah selesai

### **Untuk Peserta**
1. **Login** dengan akun Google
2. **Scan QR Code** yang ditampilkan admin
3. **Izinkan Lokasi** (opsional)
4. **Presensi Otomatis** tercatat
5. **Lihat Riwayat** presensi pribadi

## 🎨 **Design System**

### **Color Palette**
```css
/* Primary Colors */
--primary: #667eea → #764ba2
--success: #4facfe → #00f2fe  
--warning: #fa709a → #fee140
--secondary: #f093fb → #f5576c

/* Glass Effects */
--glass-bg: rgba(255, 255, 255, 0.1)
--glass-border: rgba(255, 255, 255, 0.2)
--backdrop-blur: 20px
```

### **Typography**
- **Font Family**: Inter (300, 400, 500, 600, 700, 800)
- **Heading Sizes**: 3xl, 4xl, 5xl
- **Body Text**: Base, lg, xl
- **Responsive**: Mobile-first approach

### **Components**
- **Cards**: Glassmorphism dengan rounded corners
- **Buttons**: Gradient backgrounds dengan hover effects
- **Tables**: Modern styling dengan hover animations
- **Forms**: Clean inputs dengan focus states

## 🔧 **Konfigurasi Firebase**

### **Firebase Config**
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

### **Database Structure**
```
presensi-qr/
├── kegiatan/
│   └── {sessionId}/
│       ├── nama: string
│       ├── dibuatPada: timestamp
│       └── status: 'buka' | 'tutup'
├── presensi/
│   └── {sessionId}/
│       └── peserta/
│           └── {userId}/
│               ├── nama: string
│               ├── email: string
│               ├── waktu: timestamp
│               └── lokasi: {lat, lng}
└── users/
    └── {userId}/
        └── logs/
            └── {logId}/
                ├── namaKegiatan: string
                ├── waktu: timestamp
                └── lokasi: {lat, lng}
```

## 🚀 **Fitur Advanced**

### **QR Code Management**
- **Dynamic Generation** - QR code unik per sesi
- **Download QR** - Save sebagai gambar PNG
- **Share QR** - Native sharing atau copy to clipboard
- **Auto-expire** - QR invalid setelah sesi ditutup

### **Real-time Features**
- **Live Attendance** - Update kehadiran real-time
- **Session Status** - Monitor status sesi aktif
- **User Notifications** - Feedback instan untuk user
- **Auto-sync** - Data tersinkronisasi otomatis

### **Data Management**
- **CSV Export** - Export data kehadiran
- **Attendance Analytics** - Statistik kehadiran
- **User History** - Riwayat presensi per user
- **Location Tracking** - GPS coordinates (opsional)

## 📊 **Performance & Optimization**

### **Loading Speed**
- **CDN Resources** - Tailwind CSS, Font Awesome
- **Optimized Images** - Compressed dan responsive
- **Lazy Loading** - Load komponen saat diperlukan
- **Minified Code** - JavaScript dan CSS yang dioptimasi

### **Mobile Optimization**
- **Touch-friendly** - Button sizes yang sesuai mobile
- **Responsive Images** - Adaptive image sizing
- **Progressive Enhancement** - Fitur yang semakin baik
- **Offline Support** - PWA capabilities

## 🤝 **Contributing**

Kami sangat menghargai kontribusi dari komunitas! Berikut cara berkontribusi:

### **How to Contribute**
1. **Fork** repository ini
2. **Create** branch baru (`git checkout -b feature/AmazingFeature`)
3. **Commit** perubahan (`git commit -m 'Add some AmazingFeature'`)
4. **Push** ke branch (`git push origin feature/AmazingFeature`)
5. **Open** Pull Request

### **Guidelines**
- Gunakan **conventional commits**
- Tambahkan **tests** untuk fitur baru
- Update **documentation** sesuai perubahan
- Ikuti **coding standards** yang ada

## 📝 **Changelog**

### **v2.0.0** - UI Modernization
- ✨ **New**: Glassmorphism design system
- ✨ **New**: Gradient backgrounds dan animations
- ✨ **New**: Enhanced notification system
- ✨ **New**: Download & Share QR functionality
- 🎨 **Improved**: Modern card designs
- 🎨 **Improved**: Better mobile responsiveness
- 🐛 **Fixed**: Various UI/UX improvements

### **v1.0.0** - Initial Release
- 🎯 **Core**: QR Code generation system
- 🔐 **Auth**: Google authentication
- 📱 **Mobile**: Responsive design
- 🗄️ **Database**: Firebase integration

## 📄 **License**

Distributed under the **MIT License**. See `LICENSE` for more information.

## 📞 **Support & Contact**

### **Get Help**
- 📧 **Email**: [your-email@example.com]
- 💬 **Discord**: [Discord Server Link]
- 🐛 **Issues**: [GitHub Issues](https://github.com/i-go-on/presensi-qr/issues)

### **Community**
- 🌟 **Star** repository ini jika bermanfaat
- 🔗 **Share** dengan teman dan kolega
- 📢 **Feedback** sangat dihargai

---

<div align="center">

**⭐ Star repository ini jika bermanfaat! ⭐**

**Made with ❤️ by [Your Name]**

[![GitHub stars](https://img.shields.io/github/stars/i-go-on/presensi-qr?style=social)](https://github.com/i-go-on/presensi-qr)
[![GitHub forks](https://img.shields.io/github/forks/i-go-on/presensi-qr?style=social)](https://github.com/i-go-on/presensi-qr)
[![GitHub issues](https://img.shields.io/github/issues/i-go-on/presensi-qr)](https://github.com/i-go-on/presensi-qr/issues)

</div>
