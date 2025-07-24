# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple web-based visualization project showcasing a global T-shirt supply chain using an interactive map. The project consists of a single HTML file that creates an immersive, animated journey through the various stages of t-shirt production, from cotton farms to retail stores.

## Project Structure

- `tshirt-supply-chain-leaflet.html` - Main application file containing the complete interactive visualization
- `README.md` - Basic project documentation

## Architecture

This is a standalone HTML application that uses:

- **Leaflet.js** - Interactive mapping library for displaying the world map and supply chain locations
- **Pure HTML/CSS/JavaScript** - No build system or framework dependencies
- **Self-contained** - All code is embedded within the single HTML file

### Key Components

1. **Map Visualization** - Uses Leaflet.js with CartoDB tiles for a clean, minimal world map
2. **Supply Chain Data** - Hardcoded array of 5 supply chain nodes (Cotton Farm → Textile Mill → Garment Factory → Distribution Hub → Retail Store)
3. **Animation System** - JavaScript-based animation engine that moves through each stage of the supply chain
4. **UI Components**:
   - Title card with project branding
   - Control panel (Start Journey, Reset, Speed Toggle)
   - Progress bar showing journey completion
   - Tier information display for current stage
   - Flow panel showing complete supply chain overview

### Data Flow

1. Supply chain nodes are defined with coordinates, descriptions, and visual properties
2. Leaflet markers are created for each location with custom styling
3. Animation system progresses through stages, updating map focus and UI elements
4. Visual connections (polylines) are drawn between consecutive stages

## Development

Since this is a static HTML file, no build process is required:

1. **Running locally**: Simply open `tshirt-supply-chain-leaflet.html` in a web browser
2. **Live server**: Use any static file server (like `python -m http.server` or VS Code Live Server extension) for development

## Making Changes

When modifying the visualization:

- **Supply chain data**: Edit the `supplyChainNodes` array to change locations, descriptions, or visual properties
- **Styling**: Modify the embedded CSS (lines 9-520) for visual customization
- **Animation**: Adjust timing and behavior in the JavaScript section (lines 560-1000)
- **Map appearance**: Change tile layers or map options in the Leaflet initialization

## External Dependencies

The project loads external resources via CDN:
- Leaflet CSS and JS (version 1.9.4)
- Google Fonts (Inter font family)
- CartoDB map tiles

All dependencies are loaded from external CDNs, so an internet connection is required for full functionality.