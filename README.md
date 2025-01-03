# Viks-swip

A lightweight, modern and feature-rich slider/carousel library with zero dependencies.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Size](https://img.shields.io/badge/size-12.4kb-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Features

- 🚀 Lightweight and performant
- 📱 Touch-enabled and responsive
- 🎨 Modern and customizable design
- ♾️ Infinite loop option
- 🖱️ Mouse wheel support
- ⌨️ Keyboard navigation
- 🔄 Autoplay with pause on hover
- 📱 Mobile-friendly with touch gestures
- 🎯 Multiple slides per view
- 🌗 Light and dark themes
- ♿ Accessibility features
- 🖼️ Lazy loading support
- 🎭 CSS3 transitions and effects

## Installation

### NPM
```bash
npm install viks-swip
```

### CDN
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/viks-swip@1.0.0/dist/viks-swip.min.css">
<script src="https://cdn.jsdelivr.net/npm/viks-swip@1.0.0/dist/viks-swip.min.js"></script>
```

## Basic Usage

### HTML Structure
```html
<div class="viks-container">
    <div class="viks-wrapper">
        <div class="viks-slide">Slide 1</div>
        <div class="viks-slide">Slide 2</div>
        <div class="viks-slide">Slide 3</div>
    </div>
</div>
```

### JavaScript Initialization
```javascript
const swiper = new ViksSwip('.viks-container', {
    // options
});
```

## Configuration Options

```javascript
const defaultOptions = {
    slideClass: 'viks-slide',
    slideActiveClass: 'viks-slide-active',
    slideDuration: 300,
    autoplay: false,
    autoplayDelay: 3000,
    loop: true,
    pauseOnHover: true,
    navigation: false,
    pagination: false,
    keyboard: true,
    mousewheel: false,
    grabCursor: true,
    touchRatio: 1,
    touchAngle: 45,
    resistance: true,
    resistanceRatio: 0.85,
    speed: 300,
    direction: 'horizontal',
    slidesPerView: 1,
    spaceBetween: 0,
    centeredSlides: false,
    initialSlide: 0,
    lazyLoading: false
};
```

## API Methods

### Navigation
```javascript
// Go to next slide
swiper.slideNext();

// Go to previous slide
swiper.slidePrev();

// Go to specific slide
swiper.slideTo(index);
```

### Control
```javascript
// Start autoplay
swiper.startAutoplay();

// Stop autoplay
swiper.stopAutoplay();

// Lock slider
swiper.lock();

// Unlock slider
swiper.unlock();

// Enable slider
swiper.enable();

// Disable slider
swiper.disable();
```

### State and Information
```javascript
// Get current slide index
swiper.getActiveIndex();

// Get real index in loop mode
swiper.getRealIndex();

// Check if it's the beginning
swiper.isBeginning();

// Check if it's the end
swiper.isEnd();

// Get progress
swiper.getProgress();
```

### Updates and Cleanup
```javascript
// Update slider dimensions
swiper.update();

// Destroy instance and cleanup
swiper.destroy();
```

## Events

The library supports various callback events:

```javascript
const swiper = new ViksSwip('.viks-container', {
    onInit: function(swiper) {
        console.log('Slider initialized');
    },
    onSlideChange: function(swiper) {
        console.log('Slide changed');
    },
    onTransitionStart: function(swiper) {
        console.log('Transition started');
    },
    onTransitionEnd: function(swiper) {
        console.log('Transition ended');
    },
    onTouchStart: function(swiper, event) {
        console.log('Touch started');
    },
    onTouchMove: function(swiper, event) {
        console.log('Touch moved');
    },
    onTouchEnd: function(swiper, event) {
        console.log('Touch ended');
    }
});
```

## Responsive Breakpoints

```javascript
const swiper = new ViksSwip('.viks-container', {
    breakpoints: {
        320: {
            slidesPerView: 1,
            spaceBetween: 10
        },
        768: {
            slidesPerView: 2,
            spaceBetween: 20
        },
        1024: {
            slidesPerView: 3,
            spaceBetween: 30
        }
    }
});
```

## Lazy Loading

Enable lazy loading for images:

```html
<div class="viks-slide">
    <img data-src="image.jpg" class="viks-lazy">
</div>
```

```javascript
const swiper = new ViksSwip('.viks-container', {
    lazyLoading: true,
    lazyLoadingClass: 'viks-lazy'
});
```

## CSS Customization

### Basic Customization
```css
/* Change active slide color */
.viks-slide-active {
    background: #f0f0f0;
}

/* Customize navigation buttons */
.viks-button-prev,
.viks-button-next {
    background: #333;
}

/* Customize pagination */
.viks-bullet-active {
    background: #007aff;
}
```

### Dark Theme
```html
<div class="viks-container viks-dark">
    <!-- slides -->
</div>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- IE 11 (basic support)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Inspired by modern slider libraries
- Uses CSS3 transforms for smooth animations
- Built with performance and usability in mind

## Support

If you find any bugs or have feature requests, please create an issue in the GitHub repository.

## Author

Viks-swip is created and maintained by [Your Name].

---

Made with ❤️ for the open-source community.