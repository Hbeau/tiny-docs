# ✨Tiny Docs✨

[Tiny Docs](https://hbeau.github.io/tiny-docs/) is a community-driven knowledge base and documentation site for modding **Tiny Glade**.  
It covers game structure, asset formats, modding tools, and troubleshooting tips to help modders customize their game.

## What is Tiny Glade?🏰

[Tiny Glade](https://store.steampowered.com/app/2198150/Tiny_Glade/) is a cozy diorama builder developed in Rust using the Bevy engine.  
While there is no official mod support, the community has discovered ways to modify assets and share custom content.

## Project Structure📁

- **docs/**: All documentation pages (Markdown)
- **site/**: Generated static site (do not edit directly)
- **mkdocs.yml**: Site configuration

## How to Contribute🤝

We welcome contributions from anyone interested in modding Tiny Glade!

### Prerequisites

To preview your changes locally, you need Python and pip installed:

- **Windows:**  
  Download and install [Python](https://www.python.org/downloads/windows/).  
  Make sure to check "Add Python to PATH" during installation.

- **Verify installation:**  
  Open Command Prompt and run:
  ```
  python --version
  pip --version
  ```

### Steps

1. **Fork this repository** and clone it locally.
2. **Edit or add Markdown files** in the `docs/` folder.
   - Follow the style and structure of existing pages.
   - Add images to the appropriate subfolder.
3. **Install MkDocs and plugins:**  
   - Install [MkDocs Material](https://squidfunk.github.io/mkdocs-material/getting-started/):
     ```
     pip install mkdocs-material
     ```
   - Install extra plugins:
     ```
     pip install mkdocs-autorefs
     ```
4. **Preview your changes** locally:
   - Run the local server:
     ```
     mkdocs serve
     ```
   - Visit `http://localhost:8000` in your browser.
5. **Submit a pull request** with a clear description of your changes.

## Contribution Guidelines📚

- Keep documentation clear and beginner-friendly.
- Use screenshots and code snippets where helpful.
- Document new discoveries or troubleshooting steps.
- Respect copyright and only share original or permitted content.
- Don't put the discord invite link into the doc.

## Community🌱

- Join the **Tiny Glade Discord** for modding help and discussion.
- Share mods and guides on [Reddit](https://www.reddit.com/r/TinyGladeMods/).

---

✨*Happy modding!*✨