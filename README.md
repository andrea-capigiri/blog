# hugo-theme-basic

Basic personal site theme styled with minimal tachyons, syntax highlighting, and blog series configuration.

## Content Types

| Type        | Description                                                                                 | Command                              |
| ----------- | ------------------------------------------------------------------------------------------- | ------------------------------------ |
| **Post**    | Used for blog posts. Posts are listed on the `/post` page.                                  | `hugo new post/<post-name>.md`       |
| **Page**    | Used for site pages.                                                                        | `hugo new <page-name>.md`            |
| **Project** | Used for project pages. Extend project list by customizing `/layouts/section/project.html`. | `hugo new project/<project-name>.md` |

## Blog post series

An extra _taxonomy_, `series`, is added to allow for the grouping of blog posts. A _Read More_ section shows at the bottom of each post within the series when two or more posts are grouped.

```toml
[taxonomies]
  category = "categories"
  series = "series"
  tag = "tags"
```

## `.Params.Menu`

Menu links are specified, in order, in the theme configuration.

For example:

```toml
[[params.menu]]
  name = "blog"
  url = "blog/"

[[params.menu]]
  name = "post series"
  url = "series/"

[[params.menu]]
  name = "about"
  url = "about/"
```

## Syntax highlighting

Syntax highlighting is provided by [highlight.js](https://highlightjs.org/). The color theme can be changed by modifying the highlight.js stylesheet in `layouts/partials/head_includes.html`.
