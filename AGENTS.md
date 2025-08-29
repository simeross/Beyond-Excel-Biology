# Agent Guidelines for beyond-excel-biology

## Build/Test Commands
- Install dependencies: `bundle install`
- Serve development: `bundle exec jekyll serve`
- Build for production: `bundle exec jekyll build`
- Test build: `bundle exec jekyll build -d test`
- No specific test suite - Jekyll builds serve as validation

## Code Style & Structure
- Jekyll static site with Ruby/Sass/HTML/Markdown
- Use Sass variables defined in `css/main.scss` for styling consistency
- SCSS files in `_sass/` directory with underscores prefix
- Follow existing naming: kebab-case for files, camelCase for Sass variables
- Use semantic HTML5 elements in layouts and includes
- Liquid templating follows Jekyll conventions
- Front matter required for all content files
- Keep line length reasonable, use 2-space indentation for YAML/SCSS
- Posts in `_posts/` with YYYY-MM-DD-title.markdown format
- Layouts in `_layouts/`, includes in `_includes/`, config in `_config.yml`

## Error Handling
- Jekyll will fail builds on syntax errors - check output carefully
- Validate YAML front matter and Liquid syntax
- Test locally with `bundle exec jekyll serve` before committing