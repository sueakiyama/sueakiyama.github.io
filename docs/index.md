---
layout: home
title: "Accueil - Le Site Web de Suika AKIYAMA"
title_for_header: "ACCUEIL"
image: https://sueakiyama.github.io/thumbnail_new.png
---

# Bienvenue sur le site web de Suika Akiyama !

秋山翠花のサイトへようこそ。まずは言語を選んでください。

Welcome to the website of Suika Akiyama! Please select your favorite language.

Bienvenue sur le site web de Suika Akiyama ! Choisissez ta langue préfère.

### 言語 / Language / Langue
- [日本語 / Japanese / Japonais](index-ja)
- [英語 / English / Anglais](index-en)
- [フランス語 / French / Français](index-fr)

<h1>Latest Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <h2 style="display:inline;"><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.date | date_to_string }}
      <br>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

<!--
You can use the [editor on GitHub](https://github.com/sueakiyama/sueakiyama.github.io/edit/main/docs/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/sueakiyama/sueakiyama.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

-->
