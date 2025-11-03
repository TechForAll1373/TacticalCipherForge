# Internal API Documentation

This document describes the internal structure and public methods of the `App` object within `script.js`. While not a library, understanding this API is useful for maintenance and contribution.

## Global Object: `App`

The `App` object is the central controller of the application, encapsulated within an IIFE.

### Methods

#### `App.init()`
Initializes the application. It checks for crypto support, caches DOM elements, binds events, and performs the initial password generation and history load. This is called once on `DOMContentLoaded`.

#### `App.generatePassword()`
The core method for generating a new cipher.
-   Reads values from UI controls (length, character sets).
-   Constructs a character pool.
-   Generates a password of the specified length, ensuring at least one character from each selected set.
-   Shuffles the result for randomness.
-   Updates the UI with the new password and its strength.

#### `App.getRandomChar(charSet)`
-   **Parameters:** `charSet` (string) - A string of characters to choose from.
-   **Returns:** A single, cryptographically secure random character from the set.
-   **Implementation:** Uses `window.crypto.getRandomValues`.

#### `App.shuffleArray(array)`
-   **Parameters:** `array` (array) - The array to shuffle.
-   **Returns:** The shuffled array.
-   **Implementation:** Fisher-Yates shuffle algorithm using `window.crypto.getRandomValues`.

#### `App.calculateEntropy(poolSize, length)`
-   **Parameters:** `poolSize` (number), `length` (number).
-   **Returns:** `number` - The calculated entropy in bits.
-   **Formula:** `length * log2(poolSize)`

#### `App.updateStrengthIndicator(entropy)`
-   **Parameters:** `entropy` (number) - The entropy value.
-   **Action:** Updates the strength bar's width, color, and text based on the entropy value.

#### `App.saveToHistory(password)`, `App.loadHistory()`, `App.renderHistory()`
Manage the local storage history log, including saving, loading, and rendering the list of past ciphers.

#### `App.showToast(message, type)`
-   **Parameters:** `message` (string), `type` ('success' | 'error').
-   **Action:** Displays a temporary toast notification to the user.
