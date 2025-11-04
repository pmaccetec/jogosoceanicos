# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**jogosoceanicos** is a Brazilian Portuguese educational web application focused on ocean conservation and marine ecosystem education. The project is a collection of interactive educational games about marine ecosystems, specifically targeting Arraial do Cabo, a coastal city in Brazil known as "The Capital of Diving in Brazil."

This is a **static web application** with no build process, package managers, or external dependencies. All games are self-contained HTML files with inline CSS and JavaScript.

## Architecture

### Technology Stack
- **Pure HTML5/CSS3/JavaScript** - No frameworks, all code is vanilla
- **Static Site** - Direct HTML file deployment, no build process required
- **Responsive Design** - Mobile-first approach with breakpoints
- **Git Version Control** - Single master branch workflow

### File Structure
```
index.html                    # Main landing page with game selection
ArrastarESoltar.html          # Drag-and-drop ecosystem game (most complex)
QuizInterativo.html           # Interactive quiz game with scoring
EscolhaCertaOuErrada.html     # True/false choice game
docs/Idéias-para-Jogos.md     # Game design documentation (Portuguese)
CNAME                         # Custom domain configuration
```

### Game Architecture Pattern
All games follow a consistent architecture:
- **Self-contained HTML files** - Each game is a complete, standalone HTML file
- **Inline CSS** - All styling embedded within `<style>` tags
- **Inline JavaScript** - All game logic embedded within `<script>` tags
- **Ocean Theme** - Consistent blue gradient backgrounds with animated bubbles
- **No External Dependencies** - Completely self-contained, works offline

## Available Games

### Currently Implemented (3/5)
1. **Arrastar e Soltar** (Drag and Drop) - Ecosystem building game
2. **Quiz Interativo** (Interactive Quiz) - Knowledge testing with scenarios
3. **Escolha Certa ou Errada** (True/False Choice) - Daily action decisions

### Planned Games (2/5)
4. **Quebra-cabeça do Oceano** (Ocean Puzzle) - Image reconstruction puzzles
5. **Cadeia Alimentar** (Food Chain) - Food web sequence learning

## Development Workflow

### No Build Process
This is a static site - development consists of direct file editing:
```bash
# Edit HTML files directly
# No compilation, bundling, or build steps required
```

### Git Operations
```bash
git add . && git commit -m "descriptive message"
git push origin master
```

### Local Development
Open HTML files directly in a browser or use a static file server:
```bash
# Python 3
python -m http.server 8000

# Node.js (if available)
npx serve .

# Or simply open index.html in a browser
```

## Code Style Guidelines

### Language and Content
- **Content Language**: Brazilian Portuguese
- **Code Language**: English for variable names, comments, and function names
- **Educational Focus**: Marine conservation, biodiversity, pollution impact

### HTML Structure
- Use semantic HTML5 elements (`<header>`, `<main>`, `<section>`, etc.)
- Maintain consistent class naming conventions across games
- Include responsive meta tags for mobile compatibility

### CSS Patterns
- Mobile-first responsive design with breakpoints at 768px and 1024px
- Consistent ocean theme: blue gradients, bubble animations
- CSS Grid and Flexbox for layouts
- Smooth transitions and hover states

### JavaScript Patterns
- Vanilla JavaScript, no frameworks
- Event-driven architecture for game interactions
- Modular functions within script tags
- Error handling for user interactions

## Important Files for Development

### Core Files
1. **`index.html`** - Main navigation and game selection hub
2. **`ArrastarESoltar.html`** - Most complex game with drag-and-drop mechanics
3. **`QuizInterativo.html`** - Interactive quiz with scoring system
4. **`EscolhaCertaOuErrada.html`** - True/false choice game mechanics

### Documentation
- **`docs/Idéias-para-Jogos.md`** - Game design concepts and learning objectives (Portuguese)

## Deployment

### Static Hosting
- Works on any static web host (GitHub Pages, Netlify, Vercel, etc.)
- Custom domain configured: `jogos.xandy.dev` (via CNAME file)
- No server-side requirements
- Cross-browser compatible (HTML5/CSS3/JavaScript)

### Domain Configuration
The `CNAME` file configures the custom domain `jogos.xandy.dev`. When deploying to GitHub Pages or similar services, ensure the domain settings match this configuration.

## Educational Context

### Target Audience
- Portuguese-speaking students and general public
- Educational expo environment (ExpoXP2025)
- Age-appropriate content for environmental education

### Learning Objectives
- Marine ecosystem relationships
- Pollution impact awareness
- Sustainable environmental practices
- Individual responsibility for ocean conservation

## Game Development Guidelines

When creating new games or modifying existing ones:

1. **Follow the self-contained HTML pattern** - Keep all code within a single HTML file
2. **Maintain ocean theme consistency** - Use blue gradients, bubble animations, marine imagery
3. **Ensure mobile responsiveness** - Test on different screen sizes
4. **Provide educational feedback** - All interactions should have learning value
5. **Use Portuguese for content** - All user-facing text should be in Brazilian Portuguese
6. **Include smooth animations** - CSS transitions for better user experience

## Common Development Commands

### Local Development
```bash
# Serve locally (Python 3)
python -m http.server 8000

# Serve locally (Node.js)
npx serve .

# Open directly in browser (no server needed)
open index.html
```

### Git Workflow
```bash
# Stage and commit changes
git add . && git commit -m "descriptive message"

# Push to origin
git push origin master

# Check remote configuration
git remote -v
```

### Testing
```bash
# No automated tests - manual browser testing required
# Test each HTML file in multiple browsers:
# - index.html
# - ArrastarESoltar.html
# - QuizInterativo.html
# - EscolhaCertaOuErrada.html
```

## Common Development Tasks

### Adding a New Game
1. Create new HTML file following the naming pattern (PascalCase.html)
2. Copy structure from existing games for consistency
3. Update `index.html` to include the new game in the selection grid
4. Add game to the planned games section in documentation

### Modifying Existing Games
- Games are independent - modifications in one don't affect others
- Maintain responsive design patterns
- Test animations and interactions across browsers
- Preserve educational messaging and Portuguese content

### Testing
- Test directly in multiple browsers (Chrome, Firefox, Safari)
- Verify mobile responsiveness on actual devices
- Check all interactive elements work properly
- Ensure educational content displays correctly in Portuguese

## Git Repository Information

- **Repository**: `pmaccetec/jogosoceanicos` on GitHub
- **Main Branch**: `master`
- **Deployment**: Static hosting via GitHub Pages with custom domain `jogos.xandy.dev`
- **No CI/CD**: Direct commits to master deploy automatically