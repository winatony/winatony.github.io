# Winston Anthony - Personal Academic Website

A professional academic portfolio website built with Jekyll and hosted on GitHub Pages.

🌐 **Live Site**: [winatony.github.io](https://winatony.github.io)

## Features

- 🎨 **Modern Academic Theme** - Clean, professional design inspired by al-folio
- 🌙 **Dark Mode Toggle** - Light/dark theme with persistent preference
- 📱 **Fully Responsive** - Mobile-friendly with hamburger navigation
- ✨ **Page Transitions** - Smooth animated transitions between pages
- 📊 **GitHub Integration** - Dynamic repository listing and activity chart
- 📚 **Publications** - Google Scholar integration with citations
- 📰 **News Feed** - Latest updates and announcements

## Directory Structure

```
winatony.github.io/
├── _config.yml           # Jekyll configuration & site settings
├── Gemfile               # Ruby dependencies
├── index.markdown        # Redirects to /about/
│
├── _data/                # Data files (YAML)
│   ├── cv.yml            # CV data (education, work, skills, awards)
│   └── publications.yml  # Publications list with 'selected' flags
│
├── _pages/               # Main site pages
│   ├── about.md          # Homepage with profile & selected publications
│   ├── cv.md             # Curriculum Vitae
│   ├── projects.md       # Research projects listing
│   ├── publications.md   # Full publications list
│   └── repositories.md   # GitHub repositories showcase
│
├── _layouts/             # Page templates
│   ├── default.html      # Base layout with header/footer
│   ├── about.html        # Homepage layout with profile section
│   ├── cv.html           # CV with timeline visualization
│   ├── projects.html     # Projects grid layout
│   ├── project.html      # Individual project page
│   ├── publications.html # Publications list with filtering
│   ├── repositories.html # GitHub repos with API integration
│   ├── page.html         # Generic page layout
│   └── post.html         # Blog post layout
│
├── _includes/            # Reusable components
│   ├── head.html         # Meta tags, fonts, CSS
│   ├── header.html       # Navigation with dark mode toggle
│   ├── footer.html       # Footer with social links
│   └── scripts.html      # JavaScript (theme, mobile menu)
│
├── _projects/            # Individual project pages
│   ├── 01-human-virome.md
│   ├── 02-space-biology.md
│   ├── 03-antibiotics-microbiome.md
│   └── 04-synthetic-biology.md
│
├── _news/                # News announcements
│   ├── 2022-cell-reports.md
│   ├── 2024-nasa-funding.md
│   └── 2024-nmdc-metadata.md
│
├── assets/
│   ├── css/
│   │   └── main.scss     # All styles (CSS variables, dark mode)
│   ├── img/              # Optimized images
│   ├── images/           # Original images
│   └── pdf/              # PDF documents (papers, CV)
│
└── _site/                # Generated site (not in git)
```

## Customization Guide

### Site Configuration

Edit `_config.yml` to update:
```yaml
title: "Your Name"
email: your.email@example.com
github_username: yourusername
google_scholar_id: YOUR_ID
```

### Managing Content

#### Publications (`_data/publications.yml`)
```yaml
- title: "Paper Title"
  authors: "Author, A., Author, B."
  venue: "Journal Name"
  year: 2024
  doi: "10.xxxx/xxxxx"
  pdf: "/assets/pdf/paper.pdf"
  selected: true   # ← Set to true to feature on homepage
```

#### CV (`_data/cv.yml`)
```yaml
education:
  - degree: "Ph.D."
    field: "Your Field"
    institution: "University Name"
    year: "2020"
    
work:
  - position: "Job Title"
    company: "Company Name"
    dates: "2020 - Present"
    description: "Job description..."
```

#### Projects (`_projects/`)
Create new markdown files with front matter:
```yaml
---
layout: project
title: "Project Title"
description: "Brief description"
image: /assets/img/project.jpg
category: research
order: 1
---

Project content in markdown...
```

#### News (`_news/`)
```yaml
---
date: 2024-01-15
title: "News Title"
link: "https://optional-link.com"
---
```

#### Featured Repositories (`_pages/repositories.md`)
```yaml
featured_repos:
  - owner: OrganizationName
    name: repo-name
    highlight: |
      Your contribution description here...
```

### Styling

All styles are in `assets/css/main.scss`:
- **CSS Variables**: Colors, fonts, spacing at `:root`
- **Dark Mode**: `[data-theme="dark"]` overrides
- **Responsive**: Media queries at `@media (max-width: 768px)`

### Adding New Pages

1. Create file in `_pages/` with front matter:
```yaml
---
layout: page
title: "Page Title"
permalink: /your-page/
---
```

2. Add to navigation in `_includes/header.html`

## Local Development

### Prerequisites
- Ruby (>= 2.7)
- Bundler (`gem install bundler`)

### Setup
```bash
# Install dependencies
bundle install

# Start local server
bundle exec jekyll serve

# View at http://localhost:4000
```

### Build for Production
```bash
bundle exec jekyll build
# Output in _site/
```

## Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch via GitHub Actions (`.github/workflows/jekyll.yml`).

## Technologies

- **Static Site Generator**: Jekyll 4.3
- **Hosting**: GitHub Pages
- **Styling**: SCSS with CSS Custom Properties
- **Fonts**: Inter, JetBrains Mono (Google Fonts)
- **Icons**: Inline SVGs
- **APIs**: GitHub REST API, Google Scholar (via serpapi)

## License

MIT License - See [LICENSE](LICENSE) for details.

---

Built with ❤️ using Jekyll
