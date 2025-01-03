<div align="center">
  
# 🌊 ViksSwip

[![MIT License](https://img.shields.io/badge/License-MIT-aqua.svg)](https://github.com/Vixsry/viks-animation/blob/main/LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-aqua.svg)](https://viksanimation.my.id/)
[![Follow](https://img.shields.io/badge/Follow-@viksry12-aqua.svg)](https://www.instagram.com/viksry12)

A lightweight, modern, and feature-rich JavaScript slider/carousel library with touch support.

</div>

## 🚀 Features

- 📱 Touch-enabled slider with smooth animations
- 🔄 Infinite loop support
- ⚡ Responsive and lightweight
- 🎨 Customizable navigation and pagination
- 🖼️ Lazy loading support
- 📱 Mobile-friendly with touch gestures
- ⌨️ Keyboard navigation
- 🖱️ Mousewheel support
- 🎯 Centered slides option
- 🔧 Highly configurable

## 📦 Installation

### Using NPM
```bash
npm install viks-swip
```

### Using CDN
```html
<script src="https://viksanimation.my.id/viks-swip.min.js"></script>
```

## 🎨 Basic Usage

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
const slider = new ViksSwip('.viks-container', {
  // options
  slideClass: 'viks-slide',
  slideDuration: 300,
  autoplay: true,
  loop: true
});
```

## ⚙️ Configuration Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `slideClass` | string | 'viks-slide' | CSS class for slide elements |
| `slideActiveClass` | string | 'viks-slide-active' | CSS class for active slide |
| `slideDuration` | number | 300 | Transition duration in ms |
| `autoplay` | boolean | false | Enable automatic sliding |
| `autoplayDelay` | number | 3000 | Delay between transitions |
| `loop` | boolean | true | Enable infinite loop |
| `direction` | string | 'horizontal' | Slider direction ('horizontal'/'vertical') |
| `slidesPerView` | number | 1 | Number of slides per view |
| `spaceBetween` | number | 0 | Space between slides in pixels |
| `centeredSlides` | boolean | false | Center active slide |
| `grabCursor` | boolean | true | Show grab cursor |
| `lazyLoading` | boolean | false | Enable lazy loading |

## 🎮 API Methods

### Basic Navigation
```javascript
// Go to next slide
viksSlider.slideNext();

// Go to previous slide
viksSlider.slidePrev();

// Go to specific slide
viksSlider.slideTo(2);
```

### Control Methods
```javascript
// Start autoplay
viksSlider.startAutoplay();

// Stop autoplay
viksSlider.stopAutoplay();

// Lock slider
viksSlider.lock();

// Unlock slider
viksSlider.unlock();

// Update slider
viksSlider.update();

// Destroy slider
viksSlider.destroy();
```

### State Methods
```javascript
// Get current slide index
viksSlider.getActiveIndex();

// Check if at beginning
viksSlider.isBeginning();

// Check if at end
viksSlider.isEnd();

// Get progress
viksSlider.getProgress();
```

## 🎯 Events

```javascript
const slider = new ViksSwip('.viks-container', {
  onInit: (instance) => {
    console.log('Slider initialized');
  },
  onSlideChange: (instance) => {
    console.log('Slide changed');
  },
  onTransitionStart: (instance) => {
    console.log('Transition started');
  },
  onTransitionEnd: (instance) => {
    console.log('Transition ended');
  }
});
```

## 🎨 Styling

### Basic CSS
```css
.viks-container {
  width: 100%;
  height: 300px;
  position: relative;
}

.viks-slide {
  background: aqua;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 24px;
}

.viks-slide-active {
  opacity: 1;
}
```

## 📱 Responsive Configuration

```javascript
const slider = new ViksSwip('.viks-container', {
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

## 📖 License

MIT © [VIKRI AHPAD TANTOWI](https://github.com/Vixsry/viks-animation/blob/main/LICENSE)

## 👨‍💻 Author

**VIKRI AHPAD TANTOWI**
- Website: [viksanimation.my.id](https://viksanimation.my.id/)
- Github: [@Vixsry](https://github.com/Vixsry)
- Instagram: [@viksry12](https://www.instagram.com/viksry12)
- Facebook: [Share Profile](https://www.facebook.com/share/1E17jqYu34/)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 💫 Show your support

Give a ⭐️ if this project helped you!