# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

DocsInformatique is a Jekyll-based static site that serves as a French-language educational resource for computer science topics. It's part of the maitriser.ca ecosystem, hosted at informatique.maitriser.ca, and contains curated free programming resources and documentation translated to French.

## Common Development Commands

### Jekyll Site Development
```bash
# Install dependencies (run from docs/ directory)
cd docs/
bundle install

# Serve site locally for development
bundle exec jekyll serve

# Build static site
bundle exec jekyll build

# Bootstrap environment (install bundler and dependencies)
./script/bootstrap

# Serve via script (from docs/script/)
./script/server
```

### Troubleshooting
```bash
# If you get logger errors with Ruby 3.3+, update Jekyll version
# Edit Gemfile: change jekyll version to "~> 4.3.0"
bundle update jekyll

# Update all gems to latest compatible versions
bundle update
```

### Ruby Environment Setup
```bash
# Install Ruby dependencies
gem install bundler
bundle install
```

## Architecture

### Site Structure
```
/DocsInformatique/
├── docs/                    # Jekyll site root
│   ├── _config.yml         # Jekyll configuration
│   ├── _includes/          # Reusable HTML components
│   ├── _layouts/           # Page templates
│   ├── _sass/              # Sass stylesheets with Minima theme customizations
│   ├── assets/             # Static assets (images, CSS)
│   ├── script/             # Build and development scripts
│   ├── index.md            # Homepage with comprehensive programming resource index
│   └── about.md            # About page
└── minima/                 # Local Minima theme files
```

### Content Organization
- **Homepage (`index.md`)**: Comprehensive index of free French programming resources organized by topic
- **Resource Categories**: Covers 30+ programming languages and technologies (Python, JavaScript, Git, LaTeX, etc.)
- **Content Source**: Curated from EbookFoundation/free-programming-books repository
- **Language Focus**: Quebec French terminology and translations

### Theme and Styling
- **Base Theme**: Jekyll Minima theme
- **Customizations**: Custom SASS files in `_sass/minima/` for styling overrides
- **Responsive Design**: Mobile-friendly layout with social media integration
- **Social Integration**: Twitter, GitHub, and other social platform links configured

### Domain Architecture
- **Primary Domain**: informatique.maitriser.ca
- **Parent Site**: www.maitriser.ca (main hub)
- **Sibling Sites**: bitcoin.maitriser.ca, ethereum.maitriser.ca
- **Hosting**: GitHub Pages with custom domain via CNAME

### Development Workflow
1. Edit content in Markdown files (`index.md`, `about.md`)
2. Modify layouts/includes for structural changes
3. Update SASS files for styling modifications
4. Test locally with `bundle exec jekyll serve`
5. Deploy via git push (GitHub Pages auto-deploys)

## Content Guidelines

### Resource Curation
- Focus on free, French-language programming resources
- Maintain educational value and accessibility
- Organize by programming language and technology stack
- Include books, tutorials, courses, and interactive learning platforms

### Link Management
- Verify all external links are functional and appropriate
- Prefer stable, long-term educational resources
- Include brief descriptions for each resource when helpful
- Maintain consistent formatting across all resource listings