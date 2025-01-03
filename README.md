# Viks-swip.js

A lightweight, modern JavaScript slider library that provides infinite sliding capabilities with smooth transitions and touch support. Viks-swip.js is designed to be simple to implement while offering powerful customization options.

## Features

Viks-swip.js comes with several powerful features built-in:

- Infinite/continuous sliding without interruption
- Touch and swipe support for mobile devices
- Smooth transitions and animations
- Responsive design support
- Customizable navigation controls
- Support for both image galleries and content slides
- Thumbnail navigation system
- Autoplay functionality with customizable delays
- Easy integration with Bootstrap and other CSS frameworks
- Built-in support for Font Awesome icons

## Installation

### Using NPM

```bash
npm install viks-swip
```

### Direct Download

Download the `viks-swip.js` and `viks-swip.css` files from this repository and include them in your project:

```html
<link rel="stylesheet" href="path/to/viks-swip.css">
<script src="path/to/viks-swip.js"></script>
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
    
    <!-- Optional Navigation -->
    <button class="viks-button-prev">Previous</button>
    <button class="viks-button-next">Next</button>
    
    <!-- Optional Pagination -->
    <div class="viks-pagination"></div>
</div>
```

### JavaScript Initialization

```javascript
const slider = new ViksSwip('.viks-container', {
    slideClass: 'viks-slide',
    autoplay: true,
    autoplayDelay: 3000,
    slideDuration: 300
});
```

## Configuration Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| slideClass | string | 'viks-slide' | CSS class for slide elements |
| slideActiveClass | string | 'viks-slide-active' | CSS class for active slide |
| slideDuration | number | 300 | Transition duration in milliseconds |
| autoplay | boolean | false | Enable/disable autoplay |
| autoplayDelay | number | 3000 | Delay between slides in autoplay mode |
| loop | boolean | true | Enable/disable infinite loop |

## API Methods

### Navigation Methods

```javascript
// Go to next slide
slider.next();

// Go to previous slide
slider.prev();

// Go to specific slide
slider.goTo(index);

// Stop autoplay
slider.stopAutoplay();

// Start autoplay
slider.startAutoplay();

// Destroy slider instance and clean up
slider.destroy();
```

## Image Gallery Example

Here's an example of how to create an image gallery with Viks-swip.js:

```html
<div class="viks-container">
    <div class="viks-wrapper">
        <div class="viks-slide">
            <img src="image1.jpg" alt="Image 1">
        </div>
        <div class="viks-slide">
            <img src="image2.jpg" alt="Image 2">
        </div>
        <div class="viks-slide">
            <img src="image3.jpg" alt="Image 3">
        </div>
    </div>
    
    <!-- Thumbnails -->
    <div class="thumbnail-preview">
        <img src="thumb1.jpg" class="thumbnail active">
        <img src="thumb2.jpg" class="thumbnail">
        <img src="thumb3.jpg" class="thumbnail">
    </div>
</div>
```

## Bootstrap Integration

Viks-swip.js works seamlessly with Bootstrap. Here's an example using Bootstrap cards:

```html
<div class="viks-slide">
    <div class="card">
        <img src="image.jpg" class="card-img-top">
        <div class="card-body">
            <h5 class="card-title">Slide Title</h5>
            <p class="card-text">Slide content goes here.</p>
        </div>
    </div>
</div>
```

## Event Handling

You can listen for various events:

```javascript
// Navigation button events
document.querySelector('.viks-button-next').addEventListener('click', () => {
    slider.next();
});

// Thumbnail navigation
document.querySelectorAll('.thumbnail').forEach((thumb, index) => {
    thumb.addEventListener('click', () => {
        slider.goTo(index + 1);
    });
});
```

## Customizing Styles

The slider can be customized using CSS variables or by overriding the default classes. Here's an example of customizing the navigation buttons:

```css
.viks-button-next,
.viks-button-prev {
    background: rgba(255, 255, 255, 0.2);
    width: 50px;
    height: 50px;
    border-radius: 50%;
}

.viks-button-next:hover,
.viks-button-prev:hover {
    background: rgba(255, 255, 255, 0.3);
    transform: translateY(-50%) scale(1.1);
}
```

## Browser Support

Viks-swip.js supports all modern browsers including:

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - feel free to use this in your projects!

## Created By

[Your Name/Organization]

## Version History

- 1.0.0: Initial release
- 1.1.0: Added image gallery support
- 1.2.0: Added thumbnail navigation
- 1.3.0: Bootstrap integration improvements