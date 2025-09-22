Create a mobile friendly Python website running on a Dockerfile using TailwindCSS for Google Cloud Run which uses Google Drive for storage with the following features. The top level folder is /philosophy/ and Page files and style files are stored in folders named for their category.

User Pages (Rendered with a minimal Golang server that boots up with the main Docker instance):

An index page which shows all of the different pages grouped by category, with buttons in boxes. Each category is stylized by the same style file as that category's pages. Its style is the width of the whole page.

Each page selectable from this page renders the markdown inside of its google drive file, in the style given by the category.

Editing pages:
An editing index page which shows all of the different pages under /edit/ which shows all of the categories and has a new category button. When a user clicks one of these categories, they are taken to the edit category page.

On the edit category page, the user can edit the category name, generate a style file with a prompt (the upload contains a system prompt, the user prompt, and the current style if one exists) as well as a list of pages and a new page button.

If they click a page or create a new page, they are taken to the text editor page. This page is a simple markdown editor where all changes are auto-saved to the page file. The text component is the whole page, with a title on the top. The user also has a modal dialogue to generate a component.

When the user uses this modal dialogue, they are given a prompt window. They can then type in a name, a prompt for generating a component, and generate an HTML component to insert in the middle of this markdown document when it is rendered. In the markdown file, it will simply show the text of @component/component_name