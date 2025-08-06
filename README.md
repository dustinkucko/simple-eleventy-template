# Simple Eleventy Template

A clean, minimal static site template built with [Eleventy](https://www.11ty.dev/) static site generator, featuring component-based design, Liquid templates, and Tailwind CSS.

## Features

- ⚡ **Fast**: Built with Eleventy for lightning-fast static site generation
- 🎨 **Modern Design**: Clean, professional design with Tailwind CSS (CDN)
- 📱 **Responsive**: Mobile-first design that looks great on all devices
- ♿ **Accessible**: Semantic HTML and ARIA labels for screen readers
- 🔧 **Component-Based**: Reusable Liquid components for easy customization
- 🚀 **ES Modules**: Modern JavaScript with ES Module support
- 🎯 **Zero Build Process**: No CSS compilation or build tools required
- ✨ **Animations**: Smooth scroll animations with Intersection Observer API

## Tech Stack

- **Static Site Generator**: Eleventy (11ty)
- **Templating**: Liquid templates
- **Styling**: Tailwind CSS (CDN)
- **Icons**: Lucide Icons
- **JavaScript**: ES Modules
- **Dependencies**: Minimal (only Eleventy)

## Quick Start

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm run dev
   ```

3. **Build for production**:
   ```bash
   npm run build
   ```

## Project Structure

```
src/
├── _data/
│   └── site.json          # Site configuration
├── _includes/
│   ├── components/        # Reusable components
│   │   ├── header.liquid
│   │   ├── footer.liquid
│   │   ├── service-card.liquid
│   │   └── stats.liquid
│   └── layouts/
│       └── base.liquid    # Base layout template
└── index.liquid           # Homepage
```

## Customization

### Site Configuration

Edit `src/_data/site.json` to update:
- Site name and description
- Author information
- Social media links

### Styling

The project uses Tailwind CSS via CDN for styling. All customization is done inline in the layout file:

**To modify colors, fonts, or Tailwind configuration:**
1. Edit `src/_includes/layouts/base.liquid`
2. Find the `<script>` tag with `tailwind.config`
3. Update the configuration object:

```javascript
tailwind.config = {
  theme: {
    extend: {
      colors: {
        primary: {
          500: '#your-color-here', // Change primary color
          // ... other shades
        }
      },
      fontFamily: {
        sans: ['Your-Font', 'system-ui', 'sans-serif'],
      }
    }
  }
}
```

**To add custom CSS:**
1. Add styles in the `<style>` tag in `base.liquid`
2. Keep animations and utility classes organized

**For advanced CSS needs:**
- Create CSS files in `src/assets/css/` and link them in the layout
- Consider switching to local Tailwind build process for complex customization

### Content

- Edit `src/index.liquid` for homepage content
- Modify components in `src/_includes/components/`
- Update navigation in `src/_includes/components/header.liquid`

### Components

Create new reusable components in `src/_includes/components/`:

```liquid
<!-- Example component -->
<div class="my-component">
  <h3>{{ title }}</h3>
  <p>{{ description }}</p>
</div>
```

Include them in your templates:
```liquid
{% include "components/my-component.liquid", title: "Hello", description: "World" %}
```

## Performance Features

- **Semantic HTML**: Proper heading hierarchy and landmarks
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Minimal JavaScript**: Only essential interactive features
- **Efficient CSS**: Tailwind's utility-first approach
- **Fast Loading**: Static files with minimal dependencies

## Accessibility

- Screen reader friendly with proper ARIA labels
- Keyboard navigation support
- Focus management for interactive elements
- Reduced motion support for users with vestibular disorders
- High contrast ratios and readable fonts

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- ES Modules support required
- Graceful degradation for older browsers

## License

This project is open source and available under the [MIT License](LICENSE).
