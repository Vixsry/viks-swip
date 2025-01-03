<div align="center">
  
# 🌊 VIKS SWIP JS

### Modern Infinite Slider Library for Professional Web Applications

[![Version](https://img.shields.io/badge/version-1.0.0-7FFFD4?style=for-the-badge)](https://github.com/Vixsry/viks-swip)
[![License](https://img.shields.io/badge/license-MIT-40E0D0?style=for-the-badge)](https://mit-license.org/)
[![Size](https://img.shields.io/badge/size-12.5kb_minified-48D1CC?style=for-the-badge)](https://github.com/username/viks-swip)
[![Downloads](https://img.shields.io/badge/downloads-1k/month-00CED1?style=for-the-badge)](https://github.com/username/viks-swip)

</div>

## 🚀 Overview

ViksSwip.js is a lightweight yet powerful infinite slider library that brings professional-grade carousel functionality to your web applications. Built with performance and user experience in mind, it offers smooth animations, touch support, and extensive customization options.

### Why Choose ViksSwip?

- 📦 **Lightweight**: Only 12.5KB minified
- 🎯 **Zero Dependencies**: Pure JavaScript implementation
- 📱 **Mobile-First**: Built for touch devices
- 🔥 **High Performance**: Optimized for smooth animations
- 🎨 **Customizable**: Extensive styling options
- 🔧 **Extensible**: Plugin architecture for custom features

## 📋 Table of Contents

- [Installation](#-installation)
- [Quick Start](#-quick-start)
- [Configuration](#-configuration)
- [API Reference](#-api-reference)
- [Advanced Usage](#-advanced-usage)
- [Styling Guide](#-styling-guide)
- [Browser Support](#-browser-support)
- [Contributing](#-contributing)
- [License](#-license)

## 📦 Installation

Choose your preferred installation method:

```bash
# NPM
npm install viks-swip --save

# Yarn
yarn add viks-swip

# PNPM
pnpm add viks-swip
```

### CDN Usage

```html
<!-- Development -->
<script src="https://cdn.example.com/viks-swip/1.0.0/viks-swip.js"></script>

<!-- Production -->
<script src="https://cdn.example.com/viks-swip/1.0.0/viks-swip.min.js"></script>
```

## 🚀 Quick Start

### Basic Implementation

```html
<!-- HTML Structure -->
<div class="viks-container">
    <div class="viks-wrapper">
        <div class="viks-slide">
            <img src="slide1.jpg" alt="Slide 1">
        </div>
        <div class="viks-slide">
            <img src="slide2.jpg" alt="Slide 2">
        </div>
        <div class="viks-slide">
            <img src="slide3.jpg" alt="Slide 3">
        </div>
    </div>
</div>
```

```html
<!-- Default Aqua Theme -->
<div class="viks-container">...</div>

<!-- Material Design Theme -->
<div class="viks-container viks-theme-material">...</div>

<!-- iOS Theme -->
<div class="viks-container viks-theme-ios">...</div>
```

```javascript
// Initialize with default options
const slider = new ViksSwip('.viks-container');

// Or with custom options
const sliderCustom = new ViksSwip('.viks-container', {
    autoplay: true,
    autoplayDelay: 3000,
    loop: true,
    showIndicators: true,
    showControls: true,
    slideDuration: 300
});
```

### Essential CSS

```css
/* Core Styles */
.viks-container {
    position: relative;
    width: 100%;
    overflow: hidden;
    background: #f5f5f5;
    border-radius: 8px;
}

.viks-wrapper {
    display: flex;
    transition: transform var(--slide-duration, 300ms) ease;
    height: 100%;
}

.viks-slide {
    flex: 0 0 100%;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* Aqua Theme */
.viks-theme-aqua {
    --primary-color: #00CED1;
    --secondary-color: #7FFFD4;
    --accent-color: #40E0D0;
    --background-color: #E0FFFF;
    --text-color: #008B8B;
}
```

## ⚙️ Configuration

### Default Options

```javascript
{
    slideClass: 'viks-slide',
    slideActiveClass: 'viks-slide-active',
    slideDuration: 300,
    autoplay: false,
    autoplayDelay: 3000,
    loop: true,
    showIndicators: true,
    showControls: true,
    threshold: 50,
    direction: 'horizontal',
    effect: 'slide'
}
```

### Configuration Reference

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `slideClass` | `string` | `'viks-slide'` | Class for slide elements |
| `slideActiveClass` | `string` | `'viks-slide-active'` | Class for active slide |
| `slideDuration` | `number` | `300` | Transition duration (ms) |
| `autoplay` | `boolean` | `false` | Enable autoplay |
| `autoplayDelay` | `number` | `3000` | Autoplay delay (ms) |
| `loop` | `boolean` | `true` | Enable infinite loop |
| `showIndicators` | `boolean` | `true` | Show indicators |
| `showControls` | `boolean` | `true` | Show nav controls |
| `threshold` | `number` | `50` | Swipe threshold |
| `direction` | `string` | `'horizontal'` | Slide direction |
| `effect` | `string` | `'slide'` | Transition effect |

## 🎮 API Reference

### Core Methods

```javascript
// Navigation
slider.next();               // Go to next slide
slider.prev();               // Go to previous slide
slider.goTo(index);         // Go to specific slide

// Control
slider.startAutoplay();     // Start autoplay
slider.stopAutoplay();      // Stop autoplay
slider.destroy();           // Destroy instance

// State
slider.getCurrentIndex();   // Get current slide index
slider.getSlidesCount();    // Get total slides count
slider.isAnimating();       // Check if animating
```

### Event Handling

```javascript
// Event Listeners
slider.on('slideChange', (index) => {
    console.log(`Slide changed to index: ${index}`);
});

slider.on('touchStart', (event) => {
    console.log('Touch started');
});

slider.on('touchEnd', (event) => {
    console.log('Touch ended');
});
```

## 🔥 Advanced Usage

### Custom Transitions

```javascript
// Fade effect
const fadeSlider = new ViksSwip('.slider-container', {
    effect: 'fade',
    slideDuration: 500,
    customTransition: {
        in: 'fade-in 0.5s ease',
        out: 'fade-out 0.5s ease'
    }
});

// 3D effect
const cube3DSlider = new ViksSwip('.slider-container', {
    effect: '3d-cube',
    perspective: 1000,
    slideDuration: 800
});
```

### Dynamic Content

```javascript
// Add new slide
slider.addSlide(`
    <div class="viks-slide">
        <img src="new-image.jpg" alt="New Slide">
    </div>
`);

// Remove slide
slider.removeSlide(2); // Remove third slide

// Update slide
slider.updateSlide(1, `
    <div class="viks-slide">
        <img src="updated-image.jpg" alt="Updated Slide">
    </div>
`);
```

## 🎨 Styling Guide

### Custom Themes

```css
/* Ocean Theme */
.viks-theme-ocean {
    --viks-primary: #00CED1;
    --viks-secondary: #20B2AA;
    --viks-accent: #48D1CC;
    --viks-background: #E0FFFF;
}

/* Arctic Theme */
.viks-theme-arctic {
    --viks-primary: #B0E0E6;
    --viks-secondary: #87CEEB;
    --viks-accent: #ADD8E6;
    --viks-background: #F0F8FF;
}
```

### Navigation Styling

```css
.viks-prev,
.viks-next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: var(--viks-primary);
    border: none;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.viks-prev:hover,
.viks-next:hover {
    background: var(--viks-accent);
    transform: translateY(-50%) scale(1.1);
}
```

## 🌐 Browser Support

| Browser | Version |
|---------|---------|
| Chrome | 60+ |
| Firefox | 60+ |
| Safari | 12+ |
| Edge | 79+ |
| Opera | 47+ |
| iOS Safari | 12+ |
| Android Browser | 4.4+ |

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Credits

Created with ❤️ by Vixsry

---

<div align="center">

Made with 🌊 by the Viks Swip

[Documentation](https://viksswip.dev) • [GitHub](https://github.com/username/viks-swip) • [npm](https://www.npmjs.com/package/viks-swip)

</div>