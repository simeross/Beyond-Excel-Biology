# Agent Guidelines for beyond-excel-biology

## Build/Test Commands
- Install dependencies: `bundle install`
- Serve development: `bundle exec jekyll serve`
- Build for production: `bundle exec jekyll build`
- Test build: `bundle exec jekyll build -d test`
- No specific test suite - Jekyll builds serve as validation

## Theme & Design
- **Current Theme**: Nord Theme with Aurora color enhancements
- **Color Palette**: 16 Nord colors (nord0-15) organized as:
  - Polar Night (nord0-3): Dark backgrounds
  - Snow Storm (nord4-6): Light text/backgrounds  
  - Frost (nord7-10): Blue accent colors
  - Aurora (nord11-15): Colorful highlights for tags, interactions
- **CSS Variables**: All colors defined as CSS custom properties in `style.css`
- **Both themes supported**: Dark mode (default) and light mode via `[data-theme="light"]`
- **Aurora enhancements**: Vibrant colors for tags, hover effects, gradients

## Code Style & Structure
- Jekyll static site with Ruby/Sass/HTML/Markdown
- **Main stylesheet**: `style.css` (not `css/main.scss` - uses direct CSS)
- CSS custom properties for theming consistency
- Follow existing naming: kebab-case for files, CSS variables use `--kebab-case`
- Use semantic HTML5 elements in layouts and includes
- Liquid templating follows Jekyll conventions
- Front matter required for all content files
- Keep line length reasonable, use 2-space indentation for YAML/CSS
- Posts in `_posts/` with YYYY-MM-DD-title.markdown format
- Layouts in `_layouts/`, includes in `_includes/`, config in `_config.yml`

## Error Handling
- Jekyll will fail builds on syntax errors - check output carefully
- Validate YAML front matter and Liquid syntax
- Test locally with `bundle exec jekyll serve` before committing