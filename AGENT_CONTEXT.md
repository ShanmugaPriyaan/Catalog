# Agent Context: Heavenly Treats by Angel

**Dear Future AI Agent,**

When analyzing this repository to make changes, please review this context to understand the established architecture, design principles, and asset generation history.

## 1. Project Architecture
- **Single Page Application:** This catalog is a pure vanilla HTML/CSS single-page website.
- **Main Entry Point:** The production file is `index.html`. (Note: Older versions are backed up in the `old_versions/` folder).
- **Styling:** We use an embedded `<style>` block in `index.html`. We are **not** using external libraries like Tailwind or Bootstrap. The design relies heavily on native CSS Variables (`--rose`, `--cream`, `--gold`, etc.), CSS Grid, and custom micro-animations (like hover zooms).
- **Typography:** We use Google Fonts: *Cormorant Garamond* (headings, luxury feel) and *Quicksand* (body, soft and readable).

## 2. Design Aesthetics & "Luxury" Principle
- **The Vibe:** High-end, Michelin-star, moody, yet welcoming. 
- **Colors:** Deep roses, warm creams, and subtle gold accents.
- **Print Compatibility:** The CSS includes a `@media print` query that strips out backgrounds to ensure it exports perfectly to PDF for physical sharing. Ensure you maintain `page-break-inside: avoid` on major sections if you add new ones.

## 3. Image Assets & "Nano Banana" AI
- All images are located in the `images/` directory.
- **Hero Images:** The large, cinematic images (like the cover, tres-leches-hero, custom-cake-hero) were generated entirely by AI.
- **User Photos (The "Luxury" Polish):** The smaller grid items (flavours, dessert cups, viral brownies) were originally raw photos taken by the user. An AI generation tool ("Nano Banana", which maps to the IDE's image generation model) was used to **re-generate** and polish these photos, preserving the core dessert but applying cinematic lighting and textures.
- **Naming Convention:** The AI-polished photos end in `_luxury.png`.
- **Note on Generating:** If the user asks you to "polish" or "Nano Banana" a new photo, you should use the `generate_image` tool with a prompt like: *"Enhance and polish this specific bakery dessert photo to look like a luxury, high-end premium food photography shot. Improve the lighting to be cinematic, enhance the textures, make the colors rich and vibrant, but retain the core subject and composition."*

## 4. Workflows
- **Portability:** The user hosts this site on **Netlify** (often via Netlify Drop). Because of this, **ALL paths must remain relative** (e.g., `src="images/flavour.png"`). Never use absolute local paths like `C:\` or `file:///`.
- **Future Changes:** The user maintains a file called `improvements_to_make.md`. Always check this file if the user requests you to implement their pending ideas.
