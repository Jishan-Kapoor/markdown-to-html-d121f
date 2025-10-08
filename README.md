# Markdown Previewer

## Summary
This static web application converts the markdown content in `input.md` to HTML using Marked.js library and displays it within the `#markdown-output` div. Additionally, it utilizes `highlight.js` for rendering code blocks with syntax highlighting.

## Setup
To deploy this application on GitHub Pages, follow these steps:
1. Create a new repository on GitHub.
2. Push your code to the repository.
3. Go to the repository settings.
4. Under the GitHub Pages section, choose the source branch as `main` or `master`.
5. Access the deployed page at `https://<your-username>.github.io/<repository-name>`.

## Usage
- Access the page by navigating to the GitHub Pages URL where the application is deployed.
- There are no query parameters or configuration options required.
- Key features:
  - Markdown content in `input.md` is dynamically converted to HTML.
  - Code blocks are displayed with syntax highlighting.

## Code Explanation
This application uses HTML, CSS, and JavaScript to render the markdown content. The primary libraries used are Marked.js for markdown to HTML conversion and highlight.js for syntax highlighting.

Sample code snippet for rendering markdown content using Marked.js:

```html
<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
<div id="markdown-output"></div>

<script>
  fetch('input.md')
    .then(response => response.text())
    .then(data => {
      document.getElementById('markdown-output').innerHTML = marked(data);
    });
</script>
```

## License
This project is licensed under the MIT license.