# Thomas Chia Portfolio

A modern, responsive portfolio website built with Jekyll and optimized for GitHub Pages. Features a dark theme with animated gradients, project showcases, and mobile-first design.

## 🚀 Quick Start

### Prerequisites

- Ruby 2.7+ and Bundler
- Git for version control
- GitHub account for hosting

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/new-website.git
   cd new-website
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Serve the site locally**
   ```bash
   bundle exec jekyll serve
   ```

4. **View the site**
   Open `http://localhost:4000` in your browser

### GitHub Pages Deployment

1. **Update configuration**
   - Edit `_config.yml` and change the `url` field to your GitHub Pages URL
   - Update author information and social links

2. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial portfolio setup"
   git push origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Save the settings

4. **Wait for deployment**
   - GitHub will automatically build and deploy your site
   - Check the "Actions" tab for build status
   - Your site will be available at `https://yourusername.github.io/repository-name`

## 📁 Project Structure

```
├── _config.yml           # Jekyll configuration
├── _layouts/              # Page templates
│   ├── default.html       # Base layout with header/footer
│   └── project.html       # Individual project pages
├── _includes/             # Reusable components
│   ├── header.html        # Navigation header
│   ├── footer.html        # Footer with social links
│   └── scripts.html       # JavaScript functionality
├── _sass/                 # SCSS partial files
│   ├── _variables.scss    # Color and sizing variables
│   ├── _base.scss         # Base styles and typography
│   ├── _components.scss   # Component-specific styles
│   ├── _utilities.scss    # Utility classes and media queries
│   └── _responsive.scss   # Responsive design adjustments
├── assets/css/            # Compiled CSS
│   └── main.scss          # Main SCSS file (imports partials)
├── _projects/             # Project collection (Markdown files)
│   ├── llms-clinical-trials.md
│   ├── supply-chain-optimization.md
│   ├── table-tennis-analytics.md
│   └── portfolio-website.md
├── index.html             # Homepage
├── projects.html          # Projects listing page
├── Gemfile                # Ruby dependencies
└── README.md              # This file
```

## 🎨 Customization

### Adding New Projects

1. Create a new Markdown file in `_projects/` directory:
   ```markdown
   ---
   title: "Your Project Title"
   description: "Brief description of your project"
   image: "path/to/project-image.jpg"
   technologies:
     - "Technology 1"
     - "Technology 2"
   links:
     - text: "Live Demo"
       url: "https://your-demo.com"
     - text: "GitHub"
       url: "https://github.com/username/repo"
   date: 2024-01-01
   featured: true
   ---

   # Your project content here...
   ```

2. The project will automatically appear on the projects page and homepage (if `featured: true`)

### Updating Personal Information

Edit `_config.yml` to update:
- Site title and description
- Author information
- Email address
- Social media links

### Styling Changes

The site uses SCSS for styling with the following structure:

#### SCSS Files
- **`_sass/_variables.scss`** - Colors, fonts, spacing, and other variables
- **`_sass/_base.scss`** - Base styles, typography, and fundamental elements
- **`_sass/_components.scss`** - Component-specific styles (project cards, buttons, etc.)
- **`_sass/_utilities.scss`** - Utility classes and helper styles
- **`_sass/_responsive.scss`** - Media queries and responsive adjustments
- **`assets/css/main.scss`** - Main file that imports all partials

#### Customizing Colors
Edit `_sass/_variables.scss` to change the color scheme:
```scss
$primary-bg: #0A0A0A;        // Main background color
$primary-text: #E2E8F0;      // Primary text color
$indigo-600: rgb(79, 70, 229); // Brand color
```

#### Adding Custom Styles
- Component styles → `_sass/_components.scss`
- Utility classes → `_sass/_utilities.scss`
- Responsive styles → `_sass/_responsive.scss`

### Current Color Scheme

- **Primary**: Indigo (rgb(79, 70, 229))
- **Background**: Black (#0A0A0A)
- **Text**: Slate colors for hierarchy
- **Accent**: Various gradients and transparency effects

## 🔧 Configuration

### Site Settings (`_config.yml`)

```yaml
# Required updates
title: "Your Name | Portfolio"
email: your.email@domain.com
url: "https://yourusername.github.io"

# Author information
author:
  name: "Your Name"
  github: "your-github-username"
  linkedin: "your-linkedin-username"
  twitter: "your-twitter-username"
```

### GitHub Pages Settings

Ensure these plugins are enabled in `_config.yml`:
```yaml
plugins:
  - jekyll-feed
  - jekyll-sitemap
  - jekyll-seo-tag
```

### SCSS Configuration

The SCSS compilation is configured in `_config.yml`:
```yaml
sass:
  style: compressed
  sass_dir: _sass
```

## 📱 Features

- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Animated Background**: Scroll-based gradient animations
- **Project Showcase**: Dynamic project cards with technology tags
- **SEO Optimized**: Meta tags, structured data, and semantic HTML
- **Fast Loading**: Optimized images and minimal dependencies
- **Accessible**: WCAG compliant with keyboard navigation support
- **Modular CSS**: SCSS with organized partials for maintainability

## 🔄 Maintenance

### Updating Styles

1. **Quick color changes**: Edit variables in `_sass/_variables.scss`
2. **Component updates**: Modify `_sass/_components.scss`
3. **New utility classes**: Add to `_sass/_utilities.scss`
4. **Responsive adjustments**: Update `_sass/_responsive.scss`

### Adding Blog Posts (Optional)

To add a blog section:

1. Create `_posts/` directory
2. Add post files: `YYYY-MM-DD-post-title.md`
3. Create a blog layout and listing page
4. Update navigation to include blog link

### Updating Dependencies

```bash
bundle update
```

### Local Testing

```bash
# Development server with live reload
bundle exec jekyll serve --livereload

# Build for production
bundle exec jekyll build
```

## 🚨 Troubleshooting

### Common Issues

1. **Build Failures**
   - Check Ruby version compatibility
   - Verify all required gems are installed
   - Review GitHub Actions logs for specific errors

2. **SCSS Compilation Issues**
   - Check syntax in SCSS files
   - Ensure proper variable definitions in `_variables.scss`
   - Verify import statements in `main.scss`

3. **Missing Images**
   - Ensure image paths are correct in project frontmatter
   - Use relative URLs for local images
   - Consider using placeholder services for development

4. **Styling Issues**
   - Check browser developer tools for CSS conflicts
   - Verify SCSS compilation is working
   - Ensure Tailwind CSS is loading properly

### GitHub Pages Limitations

- Custom plugins are not supported (stick to GitHub-approved plugins)
- Build time limit of 10 minutes
- Repository size limit of 1GB
- Bandwidth limit of 100GB per month

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally
5. Submit a pull request

## 📞 Support

If you encounter any issues or have questions:
- Check the [Jekyll documentation](https://jekyllrb.com/docs/)
- Review [GitHub Pages documentation](https://docs.github.com/en/pages)
- Check [SCSS documentation](https://sass-lang.com/documentation) for styling help
- Open an issue in this repository

---

Built with ❤️ using Jekyll, Tailwind CSS, SCSS, and GitHub Pages. 