
# 🎙️ Audio ↔ Base64 Converter

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/react-%2320232a.svg?style=flat&logo=react&logoColor=%2361DAFB)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

<p align="center">
  <strong>The ultimate client-side tool for encoding audio files to Base64 and decoding them back instantly.</strong>
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-how-it-works">How It Works</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-privacy--security">Privacy</a> •
  <a href="#-contributing">Contributing</a>
</p>

---

## 🚀 Overview

**Audio to Base64 Converter** is a secure, browser-based utility designed for developers and content creators. It solves the common problem of embedding audio data directly into code (JSON, XML, HTML, CSS) by converting binary audio files into Base64 data URIs.

Unlike other converters, **this tool operates 100% offline in your browser**. No files are ever uploaded to a server, ensuring maximum privacy and speed.

## ✨ Features

-   **🔒 Privacy First**: Zero server uploads. All logic runs locally using HTML5 File API and FileReader.
-   **🔄 Bidirectional Conversion**:
    -   **Encode**: Drag & drop MP3, WAV, OGG, etc., to get a Base64 string.
    -   **Decode**: Paste a Base64 string to preview and download the audio file.
-   **⚡ Instant Preview**: Listen to your decoded audio immediately with the built-in HTML5 player.
-   **📋 Smart Clipboard**: One-click copy functionality for generated strings.
-   **🎨 Modern UI/UX**: Built with Tailwind CSS, featuring a responsive design and an immersive animated galaxy background.
-   **📱 Mobile Ready**: Fully optimized for touch devices and smaller screens.

## 🛠️ Tech Stack

-   **Frontend**: React 18+, TypeScript
-   **Styling**: Tailwind CSS (Utility-first framework)
-   **Animations**: Custom CSS keyframes for galaxy effects
-   **Build Tooling**: Vite (implied via usage patterns)

## 💡 How It Works

### Encoding (Audio → Text)
1.  **Select**: User drops a file into the dropzone.
2.  **Read**: The app uses `FileReader.readAsDataURL()` to read the binary data.
3.  **Output**: The resulting Data URI (e.g., `data:audio/mp3;base64,...`) is displayed for copying.

### Decoding (Text → Audio)
1.  **Input**: User pastes a Base64 string.
2.  **Parse**: The app strips the header to isolate the Base64 data.
3.  **Convert**: `window.atob()` converts Base64 to binary string, which is then converted to a `Uint8Array`.
4.  **Blob**: A `Blob` is created and converted to a generic Object URL via `URL.createObjectURL()`.
5.  **Play/Save**: The Object URL is fed into an `<audio>` tag and a download anchor.

## 🚀 Getting Started

### Prerequisites
-   Node.js (v16+)
-   npm or yarn

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/hsinidev/audio-base64-converter.git
    cd audio-base64-converter
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Run local development server**
    ```bash
    npm run dev
    ```
    Open `http://localhost:3000` (or the port specified by your bundler) to view the app.

## 🛡️ Privacy & Security

This application is designed with a "Zero-Trust" architecture regarding server interactions. 
-   **No Backend**: There is no API server processing your files.
-   **Memory Only**: Processed files exist only in your browser's RAM during the session.
-   **GDPR/CCPA Compliant**: Since we collect no data, we are inherently compliant.

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 👨‍💻 Author

**HSINI MOHAMED**

-   Website: [doodax.com](https://doodax.com)
-   Github: [@hsinidev](https://github.com/hsinidev)
-   Email: [hsini.web@gmail.com](mailto:hsini.web@gmail.com)

---
<p align="center">
  Made with ❤️ and ☕ by Hsini
</p>
