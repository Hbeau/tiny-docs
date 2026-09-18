# ✨ Tiny Docs ✨

*By Rapunzilla*

[Tiny Docs](https://hbeau.github.io/tiny-docs/) is a community-driven knowledge base and documentation site for modding **Tiny Glade**.

It covers game structure, asset formats, modding tools, official mod support, legacy asset replacement, and troubleshooting to help modders understand and customise the game.

## What Is Tiny Glade? 🏰

[Tiny Glade](https://store.steampowered.com/app/2198150/Tiny_Glade/) is a cosy diorama builder developed in Rust using the Bevy game engine.

Tiny Glade now includes **official mod support**, including Steam Workshop integration and support for adding custom clutter items. The community also continues to document older and more advanced asset-replacement workflows.

For information about the official modding system, see the [Tiny Glade modding guide](https://pouncelight.games/tiny-glade/info/modding/).

## Project Structure 📁

- **`docs/`** — all documentation pages written in Markdown
- **`site/`** — generated static site output; do not edit this folder directly
- **`mkdocs.yml`** — MkDocs site configuration

## How to Contribute 🤝

Contributions are welcome from anyone interested in Tiny Glade modding, documentation, reverse engineering, or community tools.

### Prerequisites

To preview your changes locally, you will need Python and `pip`.

#### Windows

Download and install [Python](https://www.python.org/downloads/windows/).

During installation, make sure **Add Python to PATH** is enabled.

To verify the installation, open Command Prompt or a terminal and run:

```text
python --version
pip --version
```

### Contribution Steps

1. **Fork the repository** and clone your fork locally.

2. **Create a new branch** for your changes.

    For example:

    ```text
    docs/update-modding-guide
    ```

3. **Edit or add Markdown files** in the `docs/` folder.

    - Follow the style and structure of existing pages.
    - Add images to the appropriate `images` subfolder.
    - Keep links and file paths relative where appropriate.
    - Preview any MkDocs-specific formatting such as admonitions before submitting.

4. **Install MkDocs and the required plugins.**

    Install [MkDocs Material](https://squidfunk.github.io/mkdocs-material/getting-started/):

    ```text
    pip install mkdocs-material
    ```

    Install the additional plugin used by the project:

    ```text
    pip install mkdocs-autorefs
    ```

5. **Preview your changes locally.**

    From the repository root, run:

    ```text
    mkdocs serve
    ```

    Then open:

    ```text
    http://localhost:8000
    ```

    in your browser.

6. **Commit and push your changes** to your fork.

7. **Submit a pull request** with a clear description of what you changed and why.

## Contribution Guidelines 📚

- Keep documentation clear and beginner-friendly.
- Use screenshots, examples, and code snippets where they improve understanding.
- Document new discoveries and troubleshooting steps clearly.
- Distinguish between **official mod support** and **legacy asset-replacement methods** where relevant.
- Avoid presenting uncertain or reverse-engineered behaviour as confirmed fact.
- Respect copyright and only share original or permitted content.
- Do not add the Tiny Glade Discord invite link directly to the documentation.

## Community 🌱

- Join the **Tiny Glade Discord** through the official links provided by the game or developers for modding help and discussion.
- Share mods and guides on the [Tiny Glade Mods subreddit](https://www.reddit.com/r/TinyGladeMods/).

---

✨ *Happy modding!* ✨