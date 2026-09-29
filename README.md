Document to Markdown Converter & Reviewer
A zero-install, single-file browser application (html) designed to transcribe multi-page financial statements (PDFs, PNG, JPG, WebP) into structured GitHub-Flavored Markdown (.md) with preserved tabular structures, heading hierarchy, and reading order.

Key Features
Standalone & Zero-Install:

Single HTML file that runs entirely inside your browser (Chrome, Edge, Firefox).
No backend, server runtime, Node.js, or Python setup required.
Preserves privacy: document pages are processed directly in-memory and sent only to your configured AI provider endpoint.
Full Multi-Page Document Transcription:

Automatically detects total page count for uploaded multi-page PDFs using embedded PDF.js.
Renders each page offscreen at 2.0x scale for sharp OCR and tabular figure extraction.
Transcribes all pages sequentially into one continuous Markdown file with page navigation tags and progress reporting.
Live Formatted Markdown Preview:

Real-time side-by-side comparison between your uploaded document page and the rendered Markdown output.
Formats headings (H1–H4), numbered/bulleted lists, clean table borders, and visual page-break divider badges.
Interactive Table Review Grid:

Parses detected Markdown tables across pages into an interactive grid.
Edit cell numbers, add/delete rows and columns, and use Undo/Redo (↩, ↪).
Syncs edited tables back into their exact line positions in the Markdown document without disturbing surrounding text.
Configurable Page-Break & Source-Page Navigation:

Page Break Markers: Choose between <!-- pagebreak --> (Pandoc/Standard), --- (Horizontal Rule), \f (Form Feed), or None.
Source-Page Headings: Select ## Page {n}, ### Page {n} of {total}, **[Page {n}]**, <!-- Page {n} -->, or None.
Instant reformatting: updates live preview and raw markdown immediately upon selection.
Automated Financial Balance Checks:

Scans tables for core accounting equations: $$\text{Total Assets} = \text{Total Liabilities} + \text{Total Stockholders' Equity}$$
Identifies discrepancies and reports variance without altering extracted figures.
Themes & Session Reset:

Light / Medium / Dark Theme: Quick toggle saved to localStorage.
Reset / Clear: Instantly wipes active document state and memory to transcribe a new file.
Automated Conversion Test Suite:

Built-in test runner verifying 6 structural integrity checkpoints:
Heading hierarchy retention (H1–H4 levels).
Ordered and unordered list formatting.
Page-break divider boundary placement.
Interleaved text-and-table reading order.
Table edit & splice round-trip integrity.
Dynamic page marker and heading reformatting.
Supported AI Vision Providers
Configure your model and key in the top header:

Provider	Default Model	Custom Model Field	API Key Storage
Google Gemini	gemini-1.5-pro	Editable input (e.g. gemini-2.0-flash, gemini-1.5-flash)	Saved locally in browser localStorage
OpenAI	gpt-4o	Editable input (e.g. gpt-4o-mini, chatgpt-4o-latest)	Saved locally in browser localStorage
Groq	llama-3.2-11b-vision-preview	Editable input (e.g. llama-3.2-90b-vision-preview)	Saved locally in browser localStorage
Note: Your API keys remain on your local machine and are never transmitted to any third-party server.

Quick Start Guide
Step 1: Save the File
Save the provided HTML code to your local machine as: C:\financial_converter.html (or any folder of your choice).

Step 2: Open in Browser
Double-click financial_converter.html or open it with Google Chrome, Microsoft Edge, or Mozilla Firefox.

Step 3: Enter Your Model & API Key
Select your vision provider from the dropdown (Google Gemini, OpenAI, or Groq).
Enter or edit your preferred vision model name.
Paste your API key and click Save Config.
Step 4: Upload & Transcribe
Drag and drop your financial statement (PDF or image) onto the dropzone.
Select your desired export options (page-break marker and heading style) from the top bar.
Click ⚡ Transcribe Entire Document (All Pages).
Watch real-time progress as each page renders and populates the Live Formatted Preview.
Step 5: Review & Save
Compare the live Markdown side-by-side with the original document.
If any tabular figures need adjustment, switch to Table Grid Review, select the table, edit the cell, and click Sync Table into Document.
Check the Financial Checks tab to verify balance sheet totals.
Click 💾 Save to Local Drive (.md) to save the completed file to your local computer (supports direct native file picking or automated download).
