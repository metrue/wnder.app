# Wnder Landing Page

Professional landing page for Wnder - the AI-powered virtual tour guide app.

## Overview

This is the marketing website for Wnder located at `apps/www/` within the monorepo structure. The site showcases the app's features, provides download links, and supports multiple languages.

## Features

- **Responsive Design**: Mobile-first design that works on all devices
- **Multilingual Support**: 6 languages (English, Chinese, Spanish, French, German, Japanese)
- **Modern UI**: Clean, iOS-inspired design with smooth animations
- **SEO Optimized**: Meta tags, Open Graph, and Twitter Card support
- **Performance Focused**: Lightweight, fast-loading with optimized assets
- **Accessibility**: WCAG compliant with proper focus management

## Technology Stack

- **HTML5**: Semantic markup with proper meta tags
- **CSS3**: Modern CSS with CSS Grid, Flexbox, and custom properties
- **Vanilla JavaScript**: No frameworks, pure ES6+ for fast loading
- **Internationalization**: JSON-based translation system

## File Structure

```
apps/www/
├── index.html          # Main landing page
├── styles.css          # All CSS styles
├── script.js           # JavaScript functionality
├── README.md           # This file
└── assets/             # Images, icons, and other assets
    ├── app-store-badge.svg
    ├── google-play-badge-disabled.svg
    ├── og-image.jpg
    └── favicon.ico
```

## Supported Languages

1. **English** (en) - "Wander with Wonder"
2. **Chinese** (zh) - "漫步奇境"
3. **Spanish** (es) - "Vagar con Maravilla"  
4. **French** (fr) - "Errer avec Émerveillement"
5. **German** (de) - "Wandeln mit Wundern"
6. **Japanese** (ja) - "驚きと共に歩む"

## Development

### Local Development

1. **Simple HTTP Server**:
   ```bash
   cd apps/www
   python -m http.server 8000
   # or
   npx serve .
   ```

2. **Live Server** (VS Code Extension):
   - Install "Live Server" extension
   - Right-click `index.html` → "Open with Live Server"

### Adding New Languages

1. Add translation object to `script.js`:
   ```javascript
   const translations = {
     // ... existing languages
     'new-lang': {
       'hero.title': 'Translation here',
       // ... all other keys
     }
   };
   ```

2. Add language option to HTML:
   ```html
   <option value="new-lang">Language Name</option>
   ```

### Content Updates

- **Headlines**: Edit in HTML `data-i18n` attributes and `script.js` translations
- **Features**: Modify the features grid section in `index.html`
- **Styling**: Update `styles.css` using CSS custom properties for consistency

## Deployment

### GitHub Pages (Recommended)

1. **Setup**:
   ```bash
   # Enable GitHub Pages for the repository
   # Source: Deploy from a branch
   # Branch: main
   # Folder: /apps/www
   ```

2. **Custom Domain** (wnder.app):
   - Add `CNAME` file with `wnder.app`
   - Configure DNS A records to point to GitHub Pages IPs
   - Enable HTTPS in repository settings

### Alternative Deployments

- **Netlify**: Connect GitHub repo, set build directory to `apps/www`
- **Vercel**: Import project, set output directory to `apps/www`
- **Cloudflare Pages**: Connect repository, set build output to `apps/www`

## SEO & Analytics

### Meta Tags
- Open Graph tags for social media sharing
- Twitter Card tags for Twitter previews
- Proper meta descriptions and keywords

### Performance
- Lightweight CSS and JavaScript
- Optimized images (when added)
- Fast loading times
- Mobile-optimized

### Future Analytics Integration
The site is prepared for analytics with tracking functions:
```javascript
trackEvent('download_click', { language: 'en' });
```

## Browser Support

- **Modern Browsers**: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Mobile**: iOS Safari 14+, Chrome Mobile 90+
- **Progressive Enhancement**: Graceful fallbacks for older browsers

## Assets Needed

The following assets should be added to `apps/www/assets/`:

1. **App Store Badge**: `app-store-badge.svg`
2. **Google Play Badge**: `google-play-badge-disabled.svg` 
3. **Open Graph Image**: `og-image.jpg` (1200x630px)
4. **Favicon**: `favicon.ico`
5. **App Screenshots**: For hero section phone mockup
6. **App Icon**: High-resolution Wnder app icon

## Branding Guidelines

### Colors
- **Primary**: #007AFF (iOS Blue)
- **Secondary**: #5856D6 (iOS Purple)
- **Accent**: #FF9500 (iOS Orange)
- **Text**: #1D1D1F (Apple Black)
- **Background**: #FFFFFF (Pure White)

### Typography
- **Font Stack**: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif
- **Headings**: Bold weights (700, 600)
- **Body**: Regular weight (400)

### Voice & Tone
- **Friendly**: Approachable and welcoming
- **Professional**: Reliable and trustworthy
- **Innovative**: Cutting-edge AI technology
- **Travel-focused**: Adventure and discovery themes

## Maintenance

- **Regular Updates**: Keep translations current with app features
- **Performance Monitoring**: Check Core Web Vitals regularly
- **Content Updates**: Sync with app store listings and marketing materials
- **Analytics Review**: Monitor user engagement and download conversion rates