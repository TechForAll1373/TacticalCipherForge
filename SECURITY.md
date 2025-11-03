# Security Policy

## Supported Versions

Only the latest version of `TacticalCipherForge` is supported with security updates.

## Reporting a Vulnerability

We take the security of this project very seriously. If you discover a vulnerability, please **DO NOT** open a public issue.

Instead, please send an email to: **security@example.com** (Replace with a real contact method).

Provide as much detail as possible so we can understand and fix the issue. We will respond within 48 hours to acknowledge your report and will work on a resolution. Once a fix is available, we will credit you for your discovery (unless you wish to remain anonymous).

## Security Features

-   **Client-Side Only:** No data is ever sent to a server.
-   **Secure Randomness:** Uses the Web Crypto API (`window.crypto.getRandomValues`) for generating unpredictable ciphers.
-   **No Dependencies:** Reduces the attack surface by avoiding third-party libraries.
