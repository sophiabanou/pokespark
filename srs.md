# Software Requirements Specification (SRS)

## Project: Pokédex Web App

## Author: [Sofia-Spyridoula Banou]

## Date: [07-04-2025]

---

## 1. Introduction

### 1.1 Purpose

This document describes the software requirements for the Pokédex web application. The app is designed to provide users with detailed information about Pokémon, including their types, stats, abilities, and more.

### 1.2 Scope

The Pokédex is a responsive web app built with Astro. It will display a searchable and filterable list of Pokémon fetched from the PokéAPI. Users can view detailed Pokémon information and optionally design a team, with intelligent suggestions (e.g., missing types). Caught Pokémon can be stored locally or via account login (future feature).

---

## 2. Overall Description

### 2.1 Product Perspective

The Pokédex is a standalone web application using Astro’s hybrid static/server rendering capabilities. It consumes third-party data from the PokéAPI and is deployable on static site hosting platforms (e.g., Vercel, Netlify, GitHub Pages).

### 2.2 Product Features

- Display a list of Pokémon with name, image, and type and number.
- Search Pokémon by name or number.
- Filter Pokémon by type, region, generation.
- Detailed Pokémon page with stats, abilities, and evolution chain, more info, sprites etc.
- Ability to view shiny sprite
- On sprite click play pokemon cry
- Favorite/caught list stored locally on the device.

### 2.3 User Classes and Characteristics

- **Casual Users**: Want to browse and explore Pokémon.
- **Fans/Collectors**: Want to track their favorites, might make an account.

### 2.4 Operating Environment

- Works in modern web browsers (Chrome, Firefox, Safari, Edge).
- Responsive design for desktop, tablet, and mobile.
- Might need backend for authorization, maybe appwrite

### 2.5 Design and Implementation Constraints

- Astro framework with partial hydration.
- Uses PokéAPI (note: subject to rate limits).
- Optional backend using Appwrite for authentication and cloud storage.

### 2.6 Assumptions and Dependencies

- PokéAPI remains available and stable.
- JavaScript is enabled in the user’s browser.

---

## 3. Specific Requirements

### 3.1 Functional Requirements

- FR1: The app must fetch a list of Pokémon from PokéAPI, with pagination or infinite scrolling. The data shown on the list is: name, image, number, type.
- FR2: The user must be able to search by name and number.
- FR3: The user must be able to filter by type, area and generation.
- FR4: Clicking a Pokémon shows a details page.
- FR5: User can mark Pokémon as "caught" and "want to catch (stored in local storage / account).
- FR6: Caught and want to catch pages.

### 3.2 Non-Functional Requirements

- NFR1: The site should load within 3 seconds on standard connections.
- NFR2: The app should be responsive across all devices.
- NFR3: The UI should follow a clean and consistent visual theme.
- NFR4: The app should handle API errors gracefully.

### 3.3 User Interface Requirements

- UI1: Pokémon are displayed in a grid with images and types, names and numbers.
- UI2: Each Pokémon detail page includes:

  - Name, number, types
  - Main sprite and shiny sprite
  - Cries
  - Stats, abilities, height, weight
  - Base experience, growth rate, gender
  - Species info and multilingual names
  - Evolution chain (visualized)
  - Gallery with sprites and official artwork
  - Known locations

- UI3: Caught and want to catch pages.
- UI4: Search bar and filters are accessible at the top.

---

## 4. External Interface Requirements

### 4.1 API

- PokéAPI: `https://pokeapi.co/`
- Endpoints used: `/pokemon`, `/type`, `/evolution-chain`, etc.

### 4.2 Hardware Interfaces

- Not applicable (web only)

### 4.3 Software Interfaces

- Astro framework
- Tailwind CSS (or other CSS framework)
- Local Storage API

---

## 5. Future Enhancements (Optional)

- Pokémon comparisons (side-by-side stat comparisons)
- Catch animations or sound effects
- User accounts with cloud-synced data
- Map view to track Pokémon locations by region

---

## 6. Appendices

- A: [PokéAPI Documentation](https://pokeapi.co/docs)
- B: Wireframes or UI sketches (add if you create them)
- C: Fonts used: Inter for body, JetBrains Mono for data
- D: Color Palette: #2E2E2E, #F5F5F5, #C44536, #4A6FA5
