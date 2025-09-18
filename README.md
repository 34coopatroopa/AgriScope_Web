# AgriScope - Satellite Data Intelligence Website

A modern, responsive website showcasing satellite imagery and agricultural data intelligence. Built with clean HTML, CSS, and JavaScript.

## Features

- **Modern Design**: Clean, space-themed interface with smooth animations
- **Responsive Layout**: Works perfectly on desktop, tablet, and mobile devices
- **Interactive Gallery**: Filterable satellite imagery gallery with hover effects
- **Data Visualization**: Interactive charts showing agricultural metrics
- **Smooth Animations**: Scroll-triggered animations and transitions
- **Contact Form**: Functional contact form with validation
- **Mobile Navigation**: Hamburger menu for mobile devices

## Technologies Used

- **HTML5**: Semantic markup structure
- **CSS3**: Modern styling with CSS Grid, Flexbox, and animations
- **JavaScript**: Interactive functionality and data visualization
- **Chart.js**: Data visualization library for charts
- **Font Awesome**: Icon library
- **Google Fonts**: Inter font family

## File Structure

```
AgriScopeWeb/
├── index.html          # Main HTML file
├── styles.css          # CSS styles and animations
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## Getting Started

1. **Clone or Download**: Download all files to your local machine
2. **Open in Browser**: Simply open `index.html` in any modern web browser
3. **Local Server** (Optional): For best experience, serve files through a local server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

## Customization

### Colors and Theme
Edit the CSS variables in `styles.css` to customize colors:
```css
:root {
    --primary-color: #00d4ff;      /* Main brand color */
    --secondary-color: #ff6b35;    /* Accent color */
    --accent-color: #7c3aed;       /* Purple accent */
    --dark-bg: #0a0a0a;            /* Background color */
    /* ... other variables */
}
```

### Content Updates
- **Company Name**: Update "AgriScope" throughout the files
- **Contact Information**: Modify contact details in the contact section
- **Images**: Replace placeholder images with your actual satellite imagery
- **Data**: Update chart data and metrics in `script.js`

### Adding Real Satellite Images
1. Replace the placeholder images in the gallery section
2. Update image sources in the HTML
3. Ensure images are optimized for web (WebP format recommended)

## Sections Overview

### 1. Hero Section
- Eye-catching title with animated background
- Call-to-action buttons
- Floating particles effect

### 2. Features Section
- Six feature cards highlighting capabilities
- Hover animations and effects

### 3. Gallery Section
- Filterable image gallery
- Hover overlays with details
- Responsive grid layout

### 4. Data Insights Section
- Animated progress bars
- Interactive data chart
- Key metrics display

### 5. Contact Section
- Contact information
- Functional contact form
- Form validation

## Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Performance Features

- Optimized CSS animations
- Lazy loading for images
- Smooth scrolling
- Efficient JavaScript event handling
- Responsive images

## SEO Considerations

- Semantic HTML structure
- Meta tags for social sharing
- Alt text for images
- Proper heading hierarchy

## Future Enhancements

- Add more interactive data visualizations
- Implement real-time data updates
- Add satellite tracking features
- Include more detailed analytics
- Add user authentication for data access

## Support

For questions or customization help, please refer to the code comments or contact the development team.

## License

This project is open source and available under the MIT License.
