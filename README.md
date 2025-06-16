# Simple Find and Replace Tool

This tool allows you to perform multiple find and replace operations on `.txt` and `.docx` files directly in your browser. It's built to run on GitHub Pages.

## How to Use

1.  **Upload File:** Click the "Upload .txt or .docx file" button and select your file.
2.  **Define Pairs:**
    *   In the "Find" box, enter the text (term or sentence) you want to replace.
    *   In the "Replace with (Rich Text)" box, enter the content you want to use as a replacement. You can use rich text formatting (bold, italics, lists, etc.) provided by the editor.
    *   Click "Add another Find/Replace pair" if you need to define more replacements.
3.  **Process:** Click the "Process and Download" button.
4.  **Download:** A download link for the modified file will appear below the button.

## Features

*   Supports `.txt` files (plain text replacement).
*   Supports `.docx` files (experimental rich text replacement).
*   Multiple find/replace pairs.
*   Rich text input for replacement terms.
*   Runs entirely in the browser; no server-side processing needed.

## .docx File Processing Limitations

*   **Formatting Preservation:** When processing `.docx` files, the tool attempts to apply the rich text formatting from your "Replace with" input. However, preserving the original document's overall formatting (layouts, complex styles, headers/footers, etc.) is very challenging with client-side tools.
*   **Current Behavior for .docx:**
    *   The text content of the `.docx` file is extracted.
    *   If a "find" term is found within a paragraph of the original document, that *entire paragraph* is replaced with the content from the corresponding "Replace with (Rich Text)" editor. The formatting from the editor is applied to this new paragraph using `docx.js`'s `HtmlImporter`, which has its own limitations on what HTML it can interpret.
    *   Paragraphs from the original document that do not contain any "find" terms are carried over as plain text paragraphs, losing their original formatting.
*   Essentially, expect the output `.docx` to have the correct text changes with some basic rich text from your replacements, but it will likely not look identical to the original file's styling.

## Libraries Used

*   [Quill.js](https://quilljs.com/) - For the rich text editor.
*   [Mammoth.js](https://github.com/mwilliamson/mammoth.js) - For reading text content from `.docx` files.
*   [docx.js](https://docx.js.org/) - For generating `.docx` files.

## Disclaimer

This is a tool built for a specific use case and has known limitations, especially with `.docx` formatting. Always keep backups of your original files.
