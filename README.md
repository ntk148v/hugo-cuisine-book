<div align="center">
 <h1>Hugo Cuisine Book</h1>
 <blockquote align="center">A simple Hugo theme</blockquote>
 <p>
  <a href="https://github.com/ntk148v/hugo-cuisine-book/blob/master/LICENSE">
   <img alt="GitHub license" src="https://img.shields.io/github/license/ntk148v/hugo-cuisine-book?style=for-the-badge">
  </a>
  <a href="https://github.com/ntk148v/hugo-cuisine-book/stargazers">
            <img alt="GitHub stars" src="https://img.shields.io/github/stars/ntk148v/hugo-cuisine-book?style=for-the-badge">
        </a>
        <a href="https://gohugo.io">
            <img alt="Hugo" src="https://img.shields.io/badge/hugo-0.68-blue.svg?style=for-the-badge">
        </a>
        <a href="https://ntk148v.github.io/mammam">
            <img alt="Demo Site" src="https://img.shields.io/badge/demo-site-green.svg?style=for-the-badge">
        </a>
 </p><br>
    <p>
        <img src="./images/screenshot.png">
    </p>
</div>

- [1. Requirements](#1-requirements)
- [2. Installation](#2-installation)
  - [2.1. Install as git module](#21-install-as-git-module)
  - [2.2. Install as hugo module](#22-install-as-hugo-module)
- [3. Configuration \& Customization](#3-configuration--customization)
  - [3.1. Site configuration](#31-site-configuration)
  - [3.2. Customization](#32-customization)
- [4. Contributing](#4-contributing)

Credits:

- Highly inspired by [Recipe-Book](https://github.com/rametta/recipe-book)
- Images from [Freepik](https://freepik.com/)

## 1. Requirements

- Hugo extended version.

## 2. Installation

### 2.1. Install as git module

- Navigate to your hugo project root and run:

```bash
git submodule add https://github.com/ntk148v/hugo-cuisine-book themes/cuisine-book
```

- Run hugo (or set theme = "cuisine-book"/theme: hugo-book in configuration file)

```bash
hugo server --minify --theme cuisine-book
```

### 2.2. Install as hugo module

You can also add this theme as a Hugo module instead of a git submodule.

- Start with initializing hugo modules, if not done yet:

```bash
hugo mod init github.com/repo/path
```

- Navigate to your hugo project root and add [module] section to `config.toml`:

```bash
[module]
[[module.imports]]
path = 'github.com/ntk148v/hugo-cuisine-book'
```

- Load/update the theme module and run hugo:

```bash
hugo mod get -u
hugo server --minify
```

## 3. Configuration & Customization

### 3.1. Site configuration

- There are a few configuration options that you can add to your `config.toml` file.

```toml
# Your base url
baseURL = "http://localhost/my-title"
# Your page title
title = "my-title"
theme = "cuisine-book"
# (Optional) Set this to true to enable Author.
enableGitInfo = true

[params]
  author = "Your Name"
  description = "Describe about you"
  # (Optional) Your logo in the header navbar which has to be stored in static folder.
  # If the logo is /static/logo.png then the path would be 'logo.png'
  logo = "logo.png"
  # (Optional) Enable comments template on pages
  # By default partials/comments.html includes Disqus template
  # See https://gohugo.io/content-management/comments/#configure-disqus
  # Can be overwritten by same param in page frontmatter
  comment = true
  # Set source repository location.
  repo = 'https://github.com/ntk148v/mammam'
  # Enable 'Edit' links.
  # Disabled by default. Uncomment to enable. Requires 'repo' param.
  # Path must point to the site directory.
  editpath = 'edit/master'
  # Enable 'Add' links.
  # Disabled by default. Uncomment to enable. Requires 'repo' param.
  # Path must point to the site directory.
  newpath = 'new/master'
```

### 3.2. Customization

- Extra customization:

| File                             | Description                                                                           |
| -------------------------------- | ------------------------------------------------------------------------------------- |
| `static/favicon.png`             | Override default favicon                                                              |
| `assets/_custom.scss`            | Customize or override scss styles                                                     |
| `assets/_fonts.scss`             | Replace default font with custom fonts (e.g. local files or remote like google fonts) |
| `layouts/partials/comments.html` | Override comments.html template                                                       |

- For example, you want to change default site's background.
  - Add new background to `static/`, named it as `background.png`.
  - Add `assets/_custom.scss`

```scss
body {
  background-image: url("background.png");
}
```

## 4. Contributing

- Fork it.
- Create your feature branch (`git checkout -b my-new-feature`).
- Commit your changes (`git commit -am 'Add some feature'`).
- Push to the branch (`git push origin my-new-feature`).
- Create new Pull Request.
