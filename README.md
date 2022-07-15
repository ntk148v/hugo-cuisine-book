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
	</p><br>
</div>

- [1. Requirements](#1-requirements)
- [2. Installation](#2-installation)
	- [2.1. Install as git module](#21-install-as-git-module)
	- [2.2. Install as hugo module](#22-install-as-hugo-module)

Credits:

- Highly inspired by [Recipe-Book](https://github.com/rametta/recipe-book)
- Images from [Freepik](https://freepik.com/)

## 1. Requirements

- Hugo 0.68 or higher

## 2. Installation

### 2.1. Install as git module

- Navigate to your hugo project root and run:

```bash
git submodule add https://github.com/ntk148v/hugo-cuisine-book themes/cuisine-book
```

- Run hugo (or set theme = "cuisine-book"/theme: hugo-book in configuration file)

```bash
hugo server --minify --themecuisine-book
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
