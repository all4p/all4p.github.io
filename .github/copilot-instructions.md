# GitHub Pages Static Website - all4p.github.io

**ALWAYS follow these instructions first and only search or run additional bash commands if the information here is incomplete or found to be in error.**

This is a simple GitHub Pages static website repository containing only HTML files and documentation. The site is automatically deployed via GitHub Pages when changes are pushed to the main branch.

## Working Effectively

### Repository Structure
The repository contains minimal files:
- `README.md` - Basic repository documentation
- `index.html` - Main website homepage with documentation header
- `.github/` - GitHub configuration and workflows (if present)

### Quick Start (No Build Required)
This is a static website with no build process, dependencies, or complex setup:
- Clone the repository
- Edit HTML files directly
- Test locally using one of the serving methods below
- Commit and push changes

### Local Development and Testing

#### Method 1: Python HTTP Server (Recommended)
```bash
cd /path/to/repository
python3 -m http.server 8000
```
- **Timing**: Starts immediately (< 5 seconds)
- **Access**: Open http://localhost:8000 in browser
- **Validation**: Verify index.html loads with "My documentation" header

#### Method 2: NPX Serve (Modern Alternative)
```bash
cd /path/to/repository
npx serve . -p 3000
```
- **Timing**: First run takes 30-60 seconds to download dependencies. NEVER CANCEL during package installation.
- **Access**: Open http://localhost:3000 in browser
- **Note**: Subsequent runs are immediate

### Validation and Quality Assurance

#### HTML Validation
Always validate HTML files before committing:
```bash
npx html-validate index.html
```
- **Timing**: First run takes 30-60 seconds to download html-validate. NEVER CANCEL.
- **Expected**: Should complete without errors for valid HTML

#### Manual Testing Requirements
**CRITICAL**: After making any changes, always perform these validation steps:
1. Start local server using either method above
2. Navigate to http://localhost:PORT in browser
3. Verify the page loads correctly
4. Check that content displays as expected
5. Test any links or interactive elements
6. Verify mobile responsiveness if CSS changes were made

### Common Development Tasks

#### Adding New Pages
1. Create new `.html` file in repository root
2. Follow existing HTML structure from `index.html`
3. Test locally using serving methods above
4. Validate HTML with `npx html-validate newfile.html`

#### Editing Existing Content
1. Edit HTML files directly
2. Test changes locally immediately
3. Validate HTML syntax
4. Commit and push changes

#### Content Guidelines
- Keep HTML simple and semantic
- This repository appears to be for documentation purposes
- Maintain consistent styling with existing pages

### Git Workflow
Standard GitHub Pages workflow:
```bash
git add .
git commit -m "Description of changes"
git push origin main
```
- **Deployment**: Changes are automatically deployed via GitHub Pages
- **Timing**: Deployment typically takes 2-5 minutes after push

### Available Tools
The following tools are available in the development environment:
- Python 3.12.3 (`python3`)
- Node.js and npm (`node`, `npm`, `npx`)
- Git (`git`)
- curl for testing (`curl`)

### Troubleshooting

#### Local Server Issues
- If port 8000 is busy, use different port: `python3 -m http.server 9000`
- If npx serve fails, try using Python HTTP server instead
- Always test with `curl http://localhost:PORT/` if browser unavailable

#### HTML Issues
- Run `npx html-validate filename.html` to check syntax
- Ensure proper DOCTYPE and basic HTML structure
- Test in multiple browsers if possible

### Performance Notes
- **No build time**: This is a static site with no compilation
- **No test suite**: Manual validation only
- **No dependencies**: No package installation required
- **Immediate changes**: Edits are reflected immediately when serving locally

### GitHub Pages Specific
- Site deploys automatically from main branch
- Static files only (HTML, CSS, JS, images)
- No server-side processing available
- Custom domain configuration via repository settings

## Validation Scenarios

When making changes, always test these scenarios:

### Basic Functionality Test
1. Start local server: `python3 -m http.server 8000`
2. Open browser to http://localhost:8000
3. Verify homepage loads with expected content
4. Check that HTML structure is valid
5. Stop server with Ctrl+C

### Complete Workflow Test
1. Make a small change to index.html
2. Validate HTML: `npx html-validate index.html` (NEVER CANCEL - first run takes 60 seconds)
3. Test locally with server
4. Verify change appears correctly
5. Commit and push changes

### Expected Timings
- Local server startup: < 5 seconds
- NPX tool downloads: 30-60 seconds (NEVER CANCEL first run)
- HTML validation: < 5 seconds (after initial download)
- Git operations: < 10 seconds
- GitHub Pages deployment: 2-5 minutes

**NEVER CANCEL any npm/npx operations during package downloads - they will complete within 60 seconds.**