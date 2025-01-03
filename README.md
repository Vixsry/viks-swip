# 🌊 ViksSwip
> A powerful, lightweight infinite slider library with enhanced features

<div style="background: #E0FFFF; padding: 15px; border-radius: 5px;">
ViksSwip is a modern JavaScript slider/carousel library that provides smooth infinite scrolling, touch support, and customizable features. It's designed to be lightweight yet powerful, offering more advanced features than traditional slider libraries.
</div>

![Version](https://img.shields.io/badge/version-1.0.0-7FFFD4)
![License](https://img.shields.io/badge/license-MIT-40E0D0)
![Size](https://img.shields.io/badge/size-12.5kb-48D1CC)

## ✨ Features

- 🔄 Infinite loop scrolling
- 📱 Touch and mouse support
- ⚡ Smooth animations
- 🎮 Customizable controls
- 🔵 Progress indicators
- ⏯️ Autoplay with customizable delay
- 🎨 Fully customizable styling
- 📱 Responsive design
- 🔧 Simple API

## 📦 Installation

```bash
# Using npm
npm install viks-swip

# Using yarn
yarn add viks-swip

# Using CDN
<script src="https://cdn.example.com/viks-swip.min.js"></script>
```

## 🚀 Quick Start

### HTML Structure
```html
<div class="slider-container">
    <div class="viks-wrapper">
        <div class="viks-slide">Slide 1</div>
        <div class="viks-slide">Slide 2</div>
        <div class="viks-slide">Slide 3</div>
    </div>
</div>
```

### CSS
```css
.slider-container {
    width: 100%;
    overflow: hidden;
    position: relative;
}

.viks-wrapper {
    display: flex;
    transition: transform 300ms ease;
}

.viks-slide {
    flex: 0 0 100%;
    width: 100%;
}

/* Optional: Aqua theme styles */
.viks-prev,
.viks-next {
    background: #7FFFD4;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
}

.viks-indicator {
    width: 10px;
    height: 10px;
    background: #E0FFFF;
    border-radius: 50%;
    margin: 0 5px;
}

.viks-indicator.viks-active {
    background: #00CED1;
}
```

### JavaScript
```javascript
// Initialize the slider
const slider = new ViksSwip('.slider-container', {
    slideClass: 'viks-slide',
    autoplay: true,
    autoplayDelay: 3000,
    loop: true,
    showIndicators: true,
    showControls: true
});
```

## ⚙️ Configuration Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `slideClass` | string | 'viks-slide' | Class name for slide elements |
| `slideActiveClass` | string | 'viks-slide-active' | Class for active slide |
| `slideDuration` | number | 300 | Transition duration in milliseconds |
| `autoplay` | boolean | false | Enable/disable autoplay |
| `autoplayDelay` | number | 3000 | Delay between slides in autoplay |
| `loop` | boolean | true | Enable/disable infinite loop |
| `showIndicators` | boolean | true | Show/hide slide indicators |
| `showControls` | boolean | true | Show/hide navigation controls |

## 🎮 API Methods

```javascript
// Navigate to next slide
slider.next();

// Navigate to previous slide
slider.prev();

// Go to specific slide
slider.goTo(index);

// Stop autoplay
slider.stopAutoplay();

// Start autoplay
slider.startAutoplay();

// Destroy instance and clean up
slider.destroy();
```

## 🎯 Events

The slider responds to the following events:

- `touchstart`/`mousedown`: Initiates slide drag
- `touchmove`/`mousemove`: Handles slide movement
- `touchend`/`mouseup`: Completes slide transition
- `transitionend`: Fires after slide transition completes

## 💫 Advanced Features

### Custom Transitions
```javascript
const slider = new ViksSwip('.slider-container', {
    slideDuration: 500,  // Customize transition speed
});
```

### Dynamic Slide Addition
```javascript
// Add new slide dynamically
const newSlide = document.createElement('div');
newSlide.classList.add('viks-slide');
newSlide.innerHTML = 'New Slide';
slider.wrapper.appendChild(newSlide);
```

## 🔧 Browser Support

- ✅ Chrome 60+
- ✅ Firefox 60+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Opera 47+

## 📝 License

MIT License - feel free to use this in your projects!

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.