# Frequently Asked Questions (FAQ)

### Is the generated password truly random?

Yes. We use the `window.crypto.getRandomValues()` API, which is the industry standard for generating cryptographically secure random numbers in web browsers. It is far more secure than the typical `Math.random()` function.

### Why is there no option to save the password to a file?

For security and privacy reasons. Writing directly to the file system can introduce vulnerabilities and goes against our client-side-only philosophy. We encourage users to manually copy their ciphers to a trusted, encrypted password manager.

### Can I trust this tool for generating a master password?

Absolutely. Because the entire process runs on your machine and never touches a server, the generated cipher is as secure as your own computer. We have designed it to be a trustworthy tool for high-stakes applications.

### How is the history log stored?

The history is stored in your browser's `localStorage`. This is a local, client-side storage mechanism. It is not synchronized with any server and can be cleared at any time using the "Clear History Log" button.

### My browser doesn't support some features. What can I do?

This application uses modern web technologies. Please ensure you are using an up-to-date version of a major browser like Chrome, Firefox, Safari, or Edge for the best experience.
