# 🌐 GitDigital Content Delivery Network (CDN)

![License](https://img.shields.io/github/license/Gitdigital-products/Content-Distribution-Networks-CDNs-?color=blue)
![Build Status](https://img.shields.io/github/actions/workflow/status/Gitdigital-products/Content-Distribution-Networks-CDNs-/cdn-deploy.yml?branch=main&label=deployment)
![Last Commit](https://img.shields.io/github/last-commit/Gitdigital-products/Content-Distribution-Networks-CDNs-)
![Repo Size](https://img.shields.io/github/repo-size/Gitdigital-products/Content-Distribution-Networks-CDNs-)
![Security](https://img.shields.io/badge/security-vetted-success)

> **High-availability asset distribution for the GitDigital Fintech Ecosystem.**
---

This is the final polish. Batch 3 focuses on Developer Experience (DX) and Structure. These files turn a "folder of images" into a professional resource that other developers can actually understand and use without asking you questions.
Batch 3: Developer Experience (DX) & Governance
8. README.md (The "Front Door")
The current README is likely a placeholder. A real CDN needs to tell users where the files are and how to link them.
# GitDigital Content Delivery Network (CDN)

Global asset distribution for GitDigital fintech, KYC/AML, and infrastructure tools.

## 🚀 Usage

All assets are served via our global edge network. Use the following URL structure:

`https://cdn.gitdigital.products/[category]/[filename]`

### Example: Primary Logo
```html
<img src="[https://cdn.gitdigital.products/assets/branding/logo-main.svg](https://cdn.gitdigital.products/assets/branding/logo-main.svg)" alt="GitDigital Logo">

Example: Solana KYC SDK
<script src="[https://cdn.gitdigital.products/scripts/sdk/solana-kyc-v1.min.js](https://cdn.gitdigital.products/scripts/sdk/solana-kyc-v1.min.js)"></script>

🛠 Project Structure
 * /assets: Branding, icons, and UI elements.
 * /scripts: Production-ready JavaScript SDKs.
 * /styles: Global CSS themes and design tokens.
⚡ Performance
Assets are automatically compressed (WebP/AVIF) and minified upon push to main. Cache headers are set to immutable for 1 year to ensure maximum speed.

---

### 9. `CONTRIBUTING.md`
This sets the "house rules." If a team member wants to add a new logo, they need to know the naming conventions so the CDN doesn't become a mess.

```markdown
# Contributing to GitDigital CDN

To maintain a high-performance network, please follow these guidelines when adding assets:

### 1. File Naming
- Use `kebab-case` (e.g., `primary-logo.png`, not `PrimaryLogo.png`).
- Include version numbers for scripts: `auth-v1.js`.

### 2. Image Requirements
- **Vector:** Use `.svg` whenever possible for icons and logos.
- **Raster:** High-resolution `.png` or `.jpg`. Our CI/CD will automatically generate `.webp` versions.

### 3. Pull Request Process
1. Upload assets to the appropriate directory.
2. Update `manifest.json` to include the new asset.
3. Submit a PR for review.

10. index.html (The "Safety Guard")
If someone visits https://cdn.gitdigital.products/ directly, you don't want them seeing a 404 or a file list. This file acts as a clean landing page.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>GitDigital CDN</title>
    <style>
        body { font-family: sans-serif; display: flex; align-items: center; justify-content: center; height: 100vh; background: #0f172a; color: white; }
        .card { text-align: center; border: 1px solid #1e293b; padding: 2rem; border-radius: 8px; }
    </style>
</head>
<body>
    <div class="card">
        <h1>GitDigital Assets</h1>
        <p>This is a private Content Delivery Network.</p>
        <a href="https://github.com/Gitdigital-products" style="color: #38bdf8;">View Organization</a>
    </div>
</body>
</html>

11. .editorconfig
Ensures that everyone's code editor (VS Code, etc.) uses the same spacing and line endings so your manifest.json doesn't get messy.
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.md]
trim_trailing_whitespace = false

Final "Checklist" for Success:
 * [ ] Batch 1: Legal and Headers (CORS is the most important!).
 * [ ] Batch 2: Automation (Saves you hours of manual compression).
 * [ ] Batch 3: Docs (So you don't have to explain the link structure to every new dev).
Would you like me to help you bundle these into a single shell script that creates all these files at once in your local directory?

# Content-Distribution-Networks-CDNs-
Content Distribution Networks (CDNs):** Decentralized approaches to content delivery.
