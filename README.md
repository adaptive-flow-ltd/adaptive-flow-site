# Adaptive Flow Ltd - Company Website

Welcome to the official website repository for Adaptive Flow Ltd.

## About

This repository contains the source code for the Adaptive Flow Ltd company website. Our site showcases our services, team, and expertise in delivering adaptive solutions for modern businesses.

## Quick Start

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (Extended version recommended)
- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/) (if using npm for additional build tools)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/adaptive-flow-ltd/adaptive-flow-site.git
   cd adaptive-flow-site
   ```

2. **Initialize git submodules** (if using theme submodules)
   ```bash
   git submodule update --init --recursive
   ```

3. **Start the development server**
   ```bash
   hugo server -D
   ```

4. **View the site**
   Open [http://localhost:1313](http://localhost:1313) in your browser

## 📁 Project Structure

```
├── content/          # Site content (markdown files)
├── layouts/          # HTML templates
├── static/           # Static assets (images, CSS, JS)
├── themes/           # Hugo themes (git submodules)
├── config/           # Site configuration
├── assets/           # Assets to be processed
├── data/             # Data files
└── public/           # Generated site (don't commit)
```

## 🛠️ Building for Production

```bash
# Build the site
hugo --minify

# Output will be in ./public/
```

## 🚀 Deployment

This site is automatically deployed using GitHub Actions when changes are pushed to the `main` branch.

### Manual Deployment

For manual deployment to various platforms:

**Netlify:**
```bash
hugo --minify
# Deploy ./public/ directory
```

**AWS S3:**
```bash
hugo --minify
aws s3 sync public/ s3://your-bucket-name --delete
```

## 📝 Content Management

### Adding New Content

**New Blog Post:**
```bash
hugo new blog/your-post-title.md
```

**New Service Page:**
```bash
hugo new services/your-service.md
```

### Content Guidelines

- Use descriptive filenames
- Include proper front matter
- Optimize images before adding
- Follow the established content structure

## 🎨 Customization

### Styling
- Custom CSS: `assets/css/custom.css`
- SCSS files: `assets/scss/`

### Configuration
- Main config: `hugo.toml` or `config.yaml`
- Environment configs: `config/_default/`

## 🔧 Development Workflow

1. Create a feature branch
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes

3. Test locally
   ```bash
   hugo server -D
   ```

4. Commit and push
   ```bash
   git add .
   git commit -m "Add: your feature description"
   git push origin feature/your-feature-name
   ```

5. Create a Pull Request

## 📦 Dependencies

### Hugo Modules
If using Hugo modules, update with:
```bash
hugo mod get -u
hugo mod tidy
```

### npm Dependencies
If using npm for additional tools:
```bash
npm install
npm run build
```

## 🤝 Contributing

We welcome contributions to improve our website. Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

### Code Style

- Use semantic HTML
- Follow accessibility guidelines
- Optimize images and assets
- Write descriptive commit messages

## 📊 Performance

### Optimization Checklist

- ✅ Images optimized and properly sized
- ✅ Minified CSS and JavaScript
- ✅ Proper cache headers
- ✅ SEO metadata included
- ✅ Mobile responsive design

### Monitoring

- Google Analytics: Configured in `config.toml`
- Performance monitoring: [WebPageTest](https://www.webpagetest.org/)
- SEO: [Google Search Console](https://search.google.com/search-console)

## 🔒 Security

- All dependencies are regularly updated
- No sensitive data in repository
- Environment variables for API keys
- Regular security audits

## 📞 Support

For technical issues or questions:

- **Internal Team**: Use our Slack #website channel
- **External Contributors**: Open an issue in this repository

## 📄 License

This website is proprietary to Adaptive Flow Ltd. All rights reserved.

---

## 🏗️ Technical Stack

- **Static Site Generator**: Hugo
- **Hosting**: Custom
- **CI/CD**: GitHub Actions
- **Theme**: Docsy
- **Analytics**: Google Analytics
- **Performance**: Cloudflare CDN

## 📱 Browser Support

- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- Mobile browsers (iOS Safari, Android Chrome)

---

**Last Updated**: [Current Date]  
**Maintained by**: Adaptive Flow Ltd Development Team
