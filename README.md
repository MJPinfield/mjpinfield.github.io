# MJPinfield Portfolio

A modern, responsive personal portfolio website showcasing cybersecurity expertise and professional experience. Built with Jekyll and styled with Tailwind CSS.

🌐 **Live Site**: [mjpinfield.github.io](https://mjpinfield.github.io)

## Tech Stack

- **Static Site Generator**: Jekyll
- **Styling**: Tailwind CSS v3.3
- **Hosting**: GitHub Pages
- **Languages**: HTML, CSS, JavaScript, Liquid templates
- **Build Tools**: Ruby (Bundler), Node.js (npm)

## Features

- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Modern UI**: Clean, professional design with dark theme
- **SEO Optimized**: Jekyll SEO tags and sitemap generation
- **Fast Loading**: Optimized CSS and static site generation
- **Professional Branding**: Cybersecurity engineer focused portfolio

## Development Setup

### Prerequisites

- Ruby 2.7+ and Bundler
- Node.js 16+ and npm
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/mjpinfield/mjpinfield.github.io.git
   cd mjpinfield.github.io
   ```

2. **Install Ruby dependencies**
   ```bash
   bundle install
   ```

3. **Install Node.js dependencies**
   ```bash
   npm install
   ```

### Development Commands

- **Start development server**
  ```bash
  npm run dev
  ```
  Starts Jekyll with live reload at `http://localhost:4000`

- **Build CSS (watch mode)**
  ```bash
  npm run build-css
  ```
  Compiles Tailwind CSS and watches for changes

- **Production build**
  ```bash
  npm run build
  ```
  Builds the site for production deployment

## Project Structure

```
.
├── _config.yml          # Jekyll configuration
├── _includes/           # Reusable template components
├── _layouts/           # Page layouts
├── _site/              # Generated site (git ignored)
├── index.html          # Homepage content
├── Gemfile             # Ruby dependencies
├── package.json        # Node.js dependencies
├── tailwind.config.js  # Tailwind CSS configuration
└── README.md           # This file
```

## Content Management

### Updating Content

- **Personal Information**: Edit `_config.yml` for site-wide settings
- **Homepage**: Modify `index.html` for main content
- **Styling**: Update Tailwind classes or `tailwind.config.js`

### Adding New Pages

1. Create new HTML/Markdown files in the root directory
2. Add appropriate front matter with layout and title
3. Update navigation if needed

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch.

### Manual Deployment

```bash
# Build the site
npm run build

# Commit and push changes
git add .
git commit -m "Update site"
git push origin main
```

## Configuration

### Jekyll Settings

Key settings in `_config.yml`:
- Site title, description, and URL
- Build settings and plugins
- Collections and permalinks
- Excluded files and directories

### Tailwind CSS

Tailwind is configured in `tailwind.config.js` with:
- Custom color palette
- Typography plugin
- Forms plugin
- Responsive breakpoints

## Performance

- **Lighthouse Score**: Optimized for performance, accessibility, and SEO
- **Static Site**: Fast loading with no server-side processing
- **CSS Optimization**: Tailwind CSS purging removes unused styles
- **Image Optimization**: Responsive images and proper formats

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile responsive design
- Progressive enhancement approach

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

**MJ Pinfield** - Cybersecurity Engineer
- LinkedIn: [mjpinfield](https://linkedin.com/in/mjpinfield)
- Website: [mjpinfield.github.io](https://mjpinfield.github.io)

---

*Built with ❤️ using Jekyll and Tailwind CSS*