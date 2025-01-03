# ViksSwip

A lightweight, feature-rich JavaScript slider library with modern capabilities. ViksSwip provides smooth transitions, multiple effects, responsive design, and advanced features while maintaining high performance.

## Features

- 🎯 Multiple transition effects (slide, fade, cube)
- 📱 Touch and mouse swipe support
- 🔄 Infinite loop
- ⚡ High performance with requestAnimationFrame
- 🖼️ Lazy loading images
- 📐 Responsive breakpoints
- ⌨️ Keyboard navigation
- 🖱️ Mousewheel support
- 🎨 Parallax effects
- 🎮 Custom controls and indicators
- 🔄 Autoplay with pause on hover
- 📱 Mobile-friendly
- 🎯 Event callbacks
- ⚙️ Highly customizable

## Installation

```bash
npm install viksswip
```

Or include directly in your HTML:

```html
<script src="path/to/viks-swip.js"></script>
```

## Basic Usage

HTML Structure:
```html
<div class="slider-container">
    <div class="viks-wrapper">
        <div class="viks-slide">Slide 1</div>
        <div class="viks-slide">Slide 2</div>
        <div class="viks-slide">Slide 3</div>
    </div>
</div>
```

Basic CSS:
```css
.slider-container {
    width: 100%;
    overflow: hidden;
    position: relative;
}

.viks-wrapper {
    display: flex;
    transition: transform 0.3s ease;
}

.viks-slide {
    flex-shrink: 0;
    width: 100%;
}
```

JavaScript Initialization:
```javascript
const slider = new ViksSwip('.slider-container', {
    // options
});
```

## Configuration Options

```javascript
{
    slideClass: 'viks-slide',         // Class for slides
    slideActiveClass: 'viks-slide-active', // Class for active slide
    slideDuration: 300,               // Transition duration in ms
    autoplay: false,                  // Enable autoplay
    autoplayDelay: 3000,             // Delay between transitions
    loop: true,                       // Enable infinite loop
    showIndicators: true,             // Show pagination indicators
    showControls: true,               // Show navigation arrows
    effect: 'slide',                  // 'slide', 'fade', 'cube'
    direction: 'horizontal',          // 'horizontal', 'vertical'
    touchThreshold: 0.2,              // Swipe threshold (0-1)
    parallax: false,                  // Enable parallax effect
    keyboard: true,                   // Enable keyboard navigation
    mousewheel: false,                // Enable mousewheel navigation
    preloadImages: true,              // Preload all images
    lazy: false,                      // Enable lazy loading
    breakpoints: {                    // Responsive breakpoints
        768: {
            slideDuration: 400,
            // other options
        }
    },
    onSlideChange: null,              // Slide change callback
    onInit: null                      // Initialization callback
}
```

## Advanced Features

### Lazy Loading
Enable lazy loading for better performance:

```html
<div class="viks-slide">
    <img data-src="image.jpg" alt="Lazy loaded image">
</div>
```

```javascript
const slider = new ViksSwip('.slider-container', {
    lazy: true
});
```

### Parallax Effect
Add parallax effect to slide elements:

```html
<div class="viks-slide">
    <div data-parallax="0.5">
        This moves at half speed
    </div>
</div>
```

```javascript
const slider = new ViksSwip('.slider-container', {
    parallax: true
});
```

### Responsive Configuration
Add breakpoint-specific options:

```javascript
const slider = new ViksSwip('.slider-container', {
    slideDuration: 300,
    breakpoints: {
        768: {
            slideDuration: 400,
            effect: 'fade'
        },
        1024: {
            slideDuration: 500,
            effect: 'cube'
        }
    }
});
```

### Event Callbacks
Use callbacks for custom behavior:

```javascript
const slider = new ViksSwip('.slider-container', {
    onInit: (swiper) => {
        console.log('Slider initialized');
    },
    onSlideChange: (currentIndex, previousIndex) => {
        console.log(`Slide changed from ${previousIndex} to ${currentIndex}`);
    }
});
```

## API Methods

```javascript
// Navigate to next slide
slider.next();

// Navigate to previous slide
slider.prev();

// Go to specific slide
slider.goTo(2);

// Start autoplay
slider.startAutoplay();

// Stop autoplay
slider.stopAutoplay();

// Update configuration
slider.updateConfig({
    slideDuration: 500
});

// Refresh slider (e.g., after DOM changes)
slider.refresh();

// Destroy slider instance
slider.destroy();
```

## Custom Styling

### Navigation Arrows
```css
.viks-prev,
.viks-next {
    /* Your custom styles */
}
```

### Pagination Indicators
```css
.viks-indicators {
    /* Container styles */
}

.viks-indicator {
    /* Individual indicator styles */
}

.viks-indicator.viks-active {
    /* Active indicator styles */
}
```

### Transition Effects
```css
.viks-wrapper[data-effect="fade"] {
    /* Fade effect styles */
}

.viks-wrapper[data-effect="cube"] {
    /* Cube effect styles */
}
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- IE 11 (basic features only)

## License

MIT License - feel free to use in commercial projects.

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## Support

For issues and feature requests, please use the GitHub issues page.