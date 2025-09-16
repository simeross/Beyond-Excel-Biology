# Hugo Migration

This branch contains the complete migration from Jekyll to Hugo.

## Changes Made

1. **Configuration**: Created `hugo.yaml` with Hugo configuration equivalent to Jekyll's `_config.yml`
2. **Content**: Migrated all posts from `_posts/` to `content/posts/` with updated frontmatter
3. **Layouts**: Converted Jekyll layouts to Hugo templates:
   - `_layouts/` → `layouts/`
   - `_includes/` → `layouts/partials/`
4. **Static Assets**: Moved `style.css` to `static/` directory
5. **Templates**: Updated Liquid templating syntax to Go template syntax
6. **GitHub Actions**: Updated deployment workflow from Jekyll to Hugo
7. **RSS Feed**: Created custom RSS template for full post content
8. **Navigation**: Fixed home link to use correct baseURL

## Hugo Directory Structure

```
├── content/
│   ├── posts/           # Blog posts (was _posts/)
│   └── about.md         # About page
├── layouts/
│   ├── _default/        # Default layouts
│   │   ├── baseof.html  # Base template
│   │   ├── single.html  # Single page/post
│   │   ├── list.html    # List page
│   │   ├── taxonomy.html # Tag pages
│   │   └── terms.html   # Tags index
│   ├── partials/        # Partial templates (was _includes/)
│   └── index.html       # Home page
├── static/
│   └── style.css        # Stylesheet
└── hugo.yaml           # Hugo configuration
```

## Features Preserved

- Nord theme with Aurora color enhancements
- Dark/light mode toggle
- Tag system (now using Hugo taxonomies)
- Blog navigation by year
- RSS feed
- All existing posts and styling

## Removed Jekyll Dependencies

- Ruby/Gem dependencies
- Jekyll plugins (tag generation now handled by Hugo)
- Jekyll-specific configuration

## To Use

```bash
# Install dependencies (none needed - Hugo is single binary)
# Build site
hugo

# Serve locally
hugo server

# Deploy
hugo && rsync -av public/ your-server:/path/
```

## Performance Improvements

- Faster builds (Go vs Ruby)
- No Ruby dependencies
- Better caching
- Single binary deployment