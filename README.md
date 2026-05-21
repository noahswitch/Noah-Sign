# Noah-Sign

Noah-Sign is a browser-based PDF signing interface built as a single HTML application. It allows users to upload a PDF, place signatures and other annotation elements on any page, edit them visually, and export the final signed PDF.

## Overview

The app is designed as a client-side signing workspace for lightweight document preparation and approval flows. Users can open a PDF, navigate through pages, insert signature elements, adjust their position and style, and generate a downloadable signed document directly in the browser.

## Features

- Upload PDF documents with drag-and-drop or file picker support
- Multi-page PDF preview with page thumbnails
- Page navigation with zoom controls and fit-to-page
- Add drawn signatures
- Add typed signatures
- Add custom text blocks
- Add images
- Add date fields
- Add initials
- Drag, resize, rotate, duplicate, and delete elements
- Edit typography properties for text-based elements
- Toggle visual grid overlay for placement alignment
- Undo recent actions
- Export the edited PDF as a signed document
- Responsive dark-themed interface with left tools panel, center canvas workspace, and right properties panel

## Tech stack

This project is implemented as a single-file front-end application in:

- HTML5
- CSS3
- Vanilla JavaScript

External libraries used:

- [pdf.js](https://mozilla.github.io/pdf.js/) for PDF rendering
- [pdf-lib](https://pdf-lib.js.org/) for PDF modification and export
- Google Fonts for typography

## Interface structure

### Top navigation bar
Contains branding, zoom controls, page information, navigation buttons, grid toggle, undo, PDF upload, and export actions.

### Left sidebar
Contains document tools such as signature, text, image, date, initials, and clear actions. It also displays PDF page thumbnails for multi-page navigation.

### Main workspace
Displays the rendered PDF page and interactive overlay area where elements are placed and edited.

### Right sidebar
Shows document statistics by default and switches to a property editor when an element is selected.

### Modals
The project includes:
- A signature modal for drawn and typed signatures
- A text modal for adding custom text content

## How it works

1. Upload a PDF document.
2. The document is rendered in the workspace and thumbnails are generated.
3. Select a tool such as Signature, Text, Image, Date, or Initials.
4. Add the element to the current page.
5. Drag and edit the element visually.
6. Use the property panel to refine position, size, rotation, font, and color where applicable.
7. Export the finished document as a signed PDF.

## Signature workflow

The app supports two signature input methods:

### Draw signature
Users can draw directly on a canvas inside the signature modal. Stroke color and width can be adjusted, and the result is inserted as an image element.

### Type signature
Users can type their name/signature and choose a visual style and color. The result is inserted as a text element.

## Editable element types

The current project supports several element types:

- Signature image
- Typed signature text
- General text
- Date
- Initials
- Uploaded image

Each element can be selected and manipulated directly on the document canvas.

## Keyboard shortcuts

The code includes support for several keyboard shortcuts:

- `Ctrl/Cmd + Z` for undo
- `Ctrl/Cmd + D` for duplicate
- `Delete` or `Backspace` for delete selected element
- `Arrow Left` / `Arrow Right` for page navigation
- `+` / `-` for zoom
- `Escape` for deselect

## File structure

At the moment, the project is packaged as one file:

- `noah-sign-1.html`

This file contains:
- HTML markup
- Embedded CSS styles
- Embedded JavaScript logic

## Limitations

- The project currently runs fully in the browser and does not include authentication or user accounts
- It does not include server-side storage or audit trails
- Export focuses on visual signing/annotation, not certified digital signature standards
- Browser compatibility may vary depending on PDF rendering and file size

## Possible improvements

- Add autosave/session restore
- Add multi-user workflows
- Add signature field templates
- Add stamp elements
- Add mobile interaction improvements
- Add authentication and secure backend storage
- Add legally compliant e-sign workflow metadata
- Refactor into separate HTML, CSS, and JS files for maintainability

## Usage

Open the HTML file in a browser, upload a PDF, place signature elements, and export the final signed version.

## Author

Created by Noah.

## License / ownership

This repository may be published as an all-rights-reserved project unless you intentionally choose an open-source license. If the code is not meant for reuse, include a copyright notice and a statement that copying, modification, or redistribution is not allowed without permission.