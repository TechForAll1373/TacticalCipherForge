# Project Architecture

This document outlines the internal structure and design philosophy of the Tactical Cipher Forge.

## File Structure

TacticalCipherForge/
├── index.html # Main application entry point (HTML structure)
├── style.css # All styles, animations, and responsive design
├── script.js # Core application logic and state management
├── assets/ # Static assets like fonts or images (if any)
├── docs/ # Extended documentation
│ ├── ARCHITECTURE.md
│ └── FAQ.md
├── .gitignore
├── LICENSE
├── README.md
└── ...other metadata files


## JavaScript Architecture

The application logic is encapsulated within an Immediately Invoked Function Expression (IIFE) to prevent global scope pollution.

-   **`App` Object:** A central object that holds all methods and state.
-   **`CONFIG` Constant:** Stores immutable configuration like character sets and history key.
-   **`elements` Cache:** A dictionary of cached DOM elements for performance.
-   **Key Methods:**
    -   `generatePassword()`: The core logic for building the cipher.
    -   `getRandomChar()`: A secure wrapper around `window.crypto.getRandomValues`.
    -   `shuffleArray()`: Implements the Fisher-Yates shuffle algorithm.
    -   `calculateEntropy()`: Calculates password strength in bits.
    -   `debounce()`: A utility function to optimize performance on slider input.

## CSS Architecture

-   **CSS Variables (`:root`):** Centralized theming for colors, fonts, and spacing.
-   **BEM-like Naming:** Class names are structured for clarity and maintainability (e.g., `.control-group`, `.checkbox-item`).
-   **Mobile-First Responsive Design:** Styles are built for small screens and scaled up using media queries.
-   **Animations:** Pure CSS animations (`@keyframes`) are used for visual effects like flickering text and scanning lines to enhance the UI without impacting performance.
