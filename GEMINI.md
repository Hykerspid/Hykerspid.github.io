# Gemini Context: Personal Hugo Website (SGurtner)

This file provides context for the AI assistant about the structure and conventions of this project.

## Project Overview

This is a personal portfolio and blog website built using the **Hugo** static site generator.

*   **Framework:** Hugo (`v0.155.3` or newer).
*   **Theme:** The project uses the **[hugo-profile](https://github.com/gurusabarish/hugo-profile)** theme, included as a Git submodule in the `themes/` directory.
*   **Site Title:** SGurtner.
*   **Architecture:** Data-driven approach. Content for homepage sections is managed in `hugo.yaml`.
*   **Multilingual:** **French (`fr`) as the default**, English (`en`) as secondary.

## Building and Running

*   **Running the Local Development Server:**
    ```bash
    hugo server -D
    ```
    *Note: The project is located on the Linux filesystem (WSL) for optimal performance and hot-reload reactivity.*

*   **Building for Production:**
    ```bash
    hugo
    ```

## Development Conventions

*   **Main Page Content:** Edit **`hugo.yaml`** under `languages.fr.params` (default) or `languages.en.params`.
*   **Navigation Menu:** Currently simplified to:
    *   **About me** (Désactivable via `disableAbout`)
    *   **Projets** (Désactivable via `disableProjects`)
    *   **Resources** (Section Blog renommée, gérée dans `menu.main`)
    *   **Contact** (Désactivable via `disableContact`)
    *   *Sections Experience, Education, and Achievements are currently disabled in the navbar.*

*   **Resources (formerly Blog):**
    *   Generic sample posts have been removed.
    *   To add a new resource/article: Create a `.md` file in `content/fr/blogs/` (French) or `content/blogs/` (English).
    *   Maintain `_index.md` in both directories to define the section header.

*   **Images and Assets:** 
    *   Static files (favicon, etc.) are in the `static/` directory.
    *   **Favicon:** Configured to use `/fav.png` in `static/`.

*   **Deployment:** Automated deployment to GitHub Pages via `.github/workflows/hugo-deploy.yml` on push to the `main` branch.
