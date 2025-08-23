# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a compliance roadmap dashboard for the NStarX Platform. It consists of a single-page web application that displays compliance framework requirements, implementation phases, and progress tracking.

## Architecture

- **Frontend**: Vanilla HTML/CSS/JavaScript application
- **Data**: Static JSON file (`compliance-data.json`) containing all compliance data
- **Deployment**: Static files served directly (no build process required)

## Key Files

- `index.html`: Main dashboard interface with embedded styles and scripts
- `compliance-data.json`: All compliance framework data, requirements, phases, and glossary terms

## Development

### Running the Application
Since this is a static site, serve the files using any HTTP server:
```bash
# Using Python
python3 -m http.server 8000

# Using Node.js http-server (if installed)
npx http-server

# Or open index.html directly in a browser
```

### Modifying Compliance Data
All compliance information is stored in `compliance-data.json`. The structure includes:
- `metadata`: Platform info and versioning
- `statistics`: Dashboard metrics
- `frameworks`: Target compliance frameworks (GDPR, HIPAA, PCI DSS, etc.)
- `phases`: Implementation timeline with tasks
- `requirements`: Categorized compliance requirements
- `stakeholders`: Roles and responsibilities
- `glossary`: Compliance terminology definitions

## Code Structure

The application uses vanilla JavaScript with:
- Dynamic DOM manipulation for rendering data
- Async data loading from JSON
- Collapsible sections for better UX
- CSS Grid for responsive layouts
- No external dependencies or frameworks