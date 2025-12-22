# Brandon Heck - Personal Website

This is a personal website built with [Hugo](https://gohugo.io/), a fast and flexible static site generator.

## Prerequisites

- [Hugo](https://gohugo.io/getting-started/installing/) (extended version recommended for SCSS support)

## Getting Started

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/brandonheck/brandonheck.github.io.git
   cd brandonheck.github.io
   ```

2. Install Hugo (if not already installed):
   - macOS: `brew install hugo`
   - Linux: Check [Hugo installation guide](https://gohugo.io/getting-started/installing/)
   - Windows: Download from [Hugo releases](https://github.com/gohugoio/hugo/releases)

### Development

1. Start the Hugo development server:
   ```bash
   hugo server
   ```

2. Open your browser to `http://localhost:1313`

3. The site will automatically reload when you make changes to content or templates.

### Building for Production

To build the static site:

```bash
hugo
```

The generated site will be in the `public/` directory.

### Deployment

This site is configured for GitHub Pages. The `public/` directory contains the built static files that should be deployed.

For automated deployment with GitHub Actions, you can set up a workflow that:
1. Builds the site with `hugo`
2. Deploys the `public/` directory to the `gh-pages` branch

## Project Structure

```
.
├── archetypes/          # Content templates
├── content/             # Site content (markdown files)
├── data/                # Data files (YAML, JSON, TOML)
├── layouts/             # HTML templates
│   └── _default/        # Default templates
│       └── baseof.html # Base template
├── static/              # Static assets (CSS, JS, images, etc.)
│   ├── css/            # Stylesheets
│   ├── js/             # JavaScript files
│   ├── img/            # Images
│   └── vendor/          # Third-party libraries
├── config.yaml         # Hugo configuration
└── README.md           # This file
```

## Configuration

Site configuration is managed in `config.yaml`. Key settings include:
- Site metadata (title, description, author)
- Social media links
- Resume content (technologies, experience, education, etc.)

## Content Management

All resume content is stored in `config.yaml` under the `params` section. To update:
- Personal information: Edit `params.profile`
- Social links: Edit `params.social`
- Resume sections: Edit the respective sections in `params` (technologies, experience, education, etc.)

## Customization

### Styling

The site uses Bootstrap 4 with custom SCSS. The compiled CSS is in `static/css/resume.min.css`. 

If you need to modify styles:
1. Edit the SCSS files in the original `scss/` directory (if you want to keep them)
2. Recompile using your preferred SCSS compiler
3. Copy the compiled CSS to `static/css/`

Alternatively, you can use Hugo's built-in asset pipeline with the extended version.

### Templates

Templates are in the `layouts/` directory:
- `layouts/_default/baseof.html`: Base template with HTML structure
- `layouts/index.html`: Home page template
- `layouts/404.html`: 404 error page template

## License

MIT License - see LICENSE file for details

## Credits

- Based on the [Start Bootstrap Resume](https://startbootstrap.com/template-overviews/resume/) theme
- Built with [Hugo](https://gohugo.io/)
- Uses [Bootstrap](https://getbootstrap.com/) for styling
