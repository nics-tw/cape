# CAPE Team Site

## Hugo Theme

Hextra: https://github.com/imfing/hextra

Theme Docs: https://imfing.github.io/hextra/docs/

Hugo Docs: https://gohugo.io/documentation/

- [Organize Files](https://imfing.github.io/hextra/docs/guide/organize-files/)
- [Markdown](https://imfing.github.io/hextra/docs/guide/markdown/), supports `GitHub-style alerts`.
- [Syntax Highlighting](https://imfing.github.io/hextra/docs/guide/syntax-highlighting/)
- [LaTeX](https://imfing.github.io/hextra/docs/guide/latex/), based on `KaTeX`.
- [Diagrams](https://imfing.github.io/hextra/docs/guide/diagrams/), currently only supports `Mermaid`.
- [Shortcodes](https://imfing.github.io/hextra/docs/guide/shortcodes/), including:
  - Callout
  - Cards
  - Details
  - FileTree
  - Icon
  - Steps
  - Tabs
  - Jupyter Notebook (alpha)
  - Others (Badge, YouTube, PDF)
- [Customizing Hextra](https://imfing.github.io/hextra/docs/advanced/customization/), including:
  - Custom CSS
  - Custom Scripts
  - Custom Layouts

## Steps to add new posts

1. Create new branches for new contents via `hugo new content/_index.md`, `hugo new content/docs/_index.md` etc.
2. Optimzie images via [Clop](https://github.com/FuzzyIdeas/Clop) and store it in `static/images`.
3. Notes for TOC and images:
   - TOC: `Hextra` generates TOC based on headings, H1 is used for post title and it won't show up in TOC. TOC only shows H2 and below.
   - Images: Since our website url is not base url, e.g. `https://nics-tw.github.io/`, but relative url, e.g. `https://nics-tw.github.io/cape/`, we need to add `/cape/` when doing image insertion:
   - Marddown style: `![some pic](/cape/images/aaa.bbb)`
   - HTML style: `<p align="center"><img src="/cape/images/aaa.bbb"></p>`
4. Front matter:
   - [Layouts](https://imfing.github.io/hextra/docs/guide/organize-files/#layouts)
   - [Sidebar Navigation](https://imfing.github.io/hextra/docs/guide/organize-files/#sidebar-navigation)
   - [Breadcrumb Navigation](https://imfing.github.io/hextra/docs/guide/organize-files/#breadcrumb-navigation)
   - [LaTeX](https://imfing.github.io/hextra/docs/guide/latex/)
   - [Hugo Native](https://gohugo.io/content-management/front-matter/)
   - `next`: next post button on the end of the post, i.e. `next: docs/usage/`.
   - `prev`: previous post button on the end of the post, i.e. `prev: docs/`
5. Preview the site locally: `hugo server --gc --disableFastRender`.
   - Images won't show properly since local url is base url.
