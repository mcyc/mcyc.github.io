# Mike Chen's Portfolio Website

This repository contains the source code for my personal portfolio website, built with [Jekyll](https://jekyllrb.com/) using the [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy). It highlights selected data science, machine learning, and AI projects with polished narratives and interactive visuals.

Visit the live site at: [https://mcyc.github.io](https://mcyc.github.io)

## Features

- Clean, mobile-friendly design using Chirpy theme
- Hosted with GitHub Pages and automatically deployed via GitHub Actions
- Responsive sidebar, search, dark/light mode toggle, and PWA support
- Organized posts with tags, categories, and archives

## Project Structure

```bash
├── _posts/              # blog posts (in Markdown)
├── assets/img/          # custom images, avatar, and favicon
├── _config.yml          # site configuration
├── Gemfile              # dependencies
├── index.html           # homepage
└── ...
```

## Development

To build and preview locally:

```bash
bundle install
bundle exec jekyll serve
```

Then visit [http://localhost:4000](http://localhost:4000) to view the site.

To test a production-like build:

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

## Deployment

This site is automatically deployed via GitHub Actions. On push to `main`, the site is built and published to the `gh-pages` branch.

You can monitor deployment status under the GitHub Actions tab.

## Credits

Powered by [Jekyll](https://jekyllrb.com/) and the amazing [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy) by [Cotes Chung](https://github.com/cotes2020).

---

Feel free to explore the source code or reach out if you'd like to discuss the content, projects, or collaborate!
