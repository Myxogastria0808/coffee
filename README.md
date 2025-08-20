# coffee

**coffee** is a blog template for zola!

This template can be used **mermaid** and **katex**.

- demo site

https://zola-coffee-theme.netlify.app/

<div align="center">
  <img src="https://github.com/Myxogastria0808/coffee/blob/main/assets/coffee.webp" width="300px" height="300px" />
</div>

## Setup Environment

1. Install zola

Please install zola by referring to the following.

https://www.getzola.org/documentation/getting-started/installation/

2. Setup coffee theme

2-1. Create your blog project

```sh
zola init < your blog project >
```
Please select as follows

```sh
Welcome to Zola!
Please answer a few questions to get started quickly.
Any choices made can be changed by modifying the `config.toml` file later.
> What is the URL of your site? (https://example.com): <your blog URL>
> Do you want to enable Sass compilation? [Y/n]: y
> Do you want to enable syntax highlighting? [y/N]: y
> Do you want to build a search index of the content? [y/N]: y

Done! Your site was created in /home/hello/Desktop/coffee-sample/docs

Get started by moving into the directory and using the built-in server: `zola serve`
Visit https://www.getzola.org for the full documentation.
```

2-2. Change directory to your blog project

```sh
cd ./< your blog project >/themes/
```

2-3. Clone coffee theme to theme directory

```sh
git clone https://github.com/Myxogastria0808/coffee.git
```

2-4. Change directory to the root of your blog project

```sh
cd ..
```

2-5. Add theme setting to `config.toml` of your blog project

```toml
theme = "coffee"
```

- example

```toml
# The URL the site will be built for
base_url = "https://example.com"

# Whether to automatically compile all Sass files in the sass directory
compile_sass = true

# Whether to build a search index to be used later on by a JavaScript library
build_search_index = true

theme = "coffee"

[markdown]
# Whether to do syntax highlighting
# Theme can be customised by setting the `highlight_theme` variable to a theme supported by Zola
highlight_code = true

[extra]
# Put all your custom variables here
```

2-6. Build your blog to apply this theme

```sh
zola build
```

2-7. Add extra settings to `config.toml` of your blog project

This theme provides the following additional settings.

All settings have default values, so you only need to add the settings you want to change.

```toml
[extra.coffee] #<- CAUTION: You have to be [extra.coffee], not [extra].
# default value: 'en'
lang = "en"
# default value: 'coffee theme'
title = "coffee theme"
# default value: 'This blog is made by zola.'
description = "This blog is made by zola."
# default value: 'blog'
keyword = "blog"
# default value: 'https://raw.githubusercontent.com/Myxogastria0808/coffee/heads/main/static/favicon.ico'
shortcut_icon = "https://raw.githubusercontent.com/Myxogastria0808/coffee/heads/main/static/favicon.ico"
# default value: ''
twitter_site = ""
# default value: '@yuki_osada0808'
twitter_creator = "@yuki_osada0808"
# default value: 'https://raw.githubusercontent.com/Myxogastria0808/coffee/heads/main/static/coffee.webp'
meta_image = "https://raw.githubusercontent.com/Myxogastria0808/coffee/heads/main/static/coffee.webp"
# default value: 'coffee theme'
meta_image_alt = "coffee theme"
# default value: '512'
meta_image_width = "512"
# default value: '512'
meta_image_height = "512"

# default value is below
about = """
Hello, my name is <strong>Myxogastria0808.</strong><br/>
I created a Zola theme named <strong>"coffee"</strong>.
This template can be used <strong>mermaid</strong> and <strong>katex</strong>.
<h4>Have a nice day!</h4>
"""
# default value: 'https://raw.githubusercontent.com/Myxogastria0808/coffee/heads/main/static/coffee.webp'
about_image = "https://raw.githubusercontent.com/Myxogastria0808/coffee/heads/main/static/coffee.webp"
# default value: 'coffee theme'
about_image_alt = "coffee theme"
# default value: '512'
about_image_width = "512"
# default value: '512'
about_image_height = "512"
```

- example

```

```

3. Check your blog

```sh
zola serve
```

## Post Example

You can see the post example below.

```md
+++
title = "coffee"
date = 2025-08-19
authors = ["Myxogastria0808"]
[taxonomies]
tags = ["coffee"]
+++

The best part of my morning is the quiet moment with a steaming mug of coffee.
It's a simple, potent reminder that a new day has truly begun.
```

Please refer to the following for an actual example.

- markdown example

https://github.com/Myxogastria0808/coffee/blob/main/content/sample/index.md

- preview URL

https://zola-coffee-theme.netlify.app/sample/

## coffee Theme Specific Notation

### List of languages in Code Block

https://www.getzola.org/documentation/content/syntax-highlighting/

#### Example

````
```rs
fn main() {
    println!("Hello, world!");
}
```
````

![codeblock](https://github.com/Myxogastria0808/coffee/blob/main/assets/codeblock.png)

### Image

```
{{ image(path="/image/path") }}
```

You can add `width=int`, `height=int`, and `caption=String` as options for image shortcode.

You can see the image shortcode examples below.

- markdown example

https://github.com/Myxogastria0808/coffee/blob/main/content/sample/index.md

- preview URL

https://zola-coffee-theme.netlify.app/sample/

#### Example applying all of `width`, `height`, and `caption`

```
{{ image(path="/content/sample/image.jpg", width=1000, height=200, caption="captionの例") }}
```

![image](https://github.com/Myxogastria0808/coffee/blob/main/assets/image.png)

> [!NOTE]
> Images are automatically converted to webp, so you don't need to worry about image size.

### katex

```
$$
<katex's syntax expression>
$$
```

#### Example

```
$$
\frac{dy}{dx} + p(x) y^2 + q(x) y + r(x) = 0
$$
```

![katex](https://github.com/Myxogastria0808/coffee/blob/main/assets/katex.png)

### mermaid

```
{% mermaid() %}
<mermaid's syntax expression>
{% end %}
```

#### Example

```
{% mermaid() %}
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
{% end %}
```

![marmaid](https://github.com/Myxogastria0808/coffee/blob/main/assets/marmaid.png)

### note

```
{% note() %}
Contents of the note.
{% end %}
```

#### Example

```
{% note() %}
This is a note.
{% end %}
```

![note](https://github.com/Myxogastria0808/coffee/blob/main/assets/note.png)

### tip

```
{% tip() %}
Contents of the tip.
{% end %}
```

#### Example

```
{% tip() %}
This is a tip.
{% end %}
```

![tip](https://github.com/Myxogastria0808/coffee/blob/main/assets/tip.png)

### important

```
{% important() %}
Contents of the important.
{% end %}
```

#### Example

```
{% important() %}
This is a important.
{% end %}
```

![important](https://github.com/Myxogastria0808/coffee/blob/main/assets/important.png)

### warning

```
{% warning() %}
Contents of the warning.
{% end %}
```

#### Example

```
{% warning() %}
This is a warning.
{% end %}
```

![warning](https://github.com/Myxogastria0808/coffee/blob/main/assets/warning.png)

### caution

```
{% caution() %}
Contents of the caution
{% end %}
```

#### Example

```
{% caution() %}
This is a caution.
{% end %}
```

![caution](https://github.com/Myxogastria0808/coffee/blob/main/assets/caution.png)

## Structure of this template

The following is expressed in pseudo-HTML.

### Top page (Also serves as an article list page)

```
<base.html>
  <index.html></index.html>
</base.html>
```

### Tag list page

```
<base.html>
  <taxonomy_list.html></taxonomy_list.html>
</base.html>
```

### List of specific tags page

```
<base.html>
  <taxonomy_single.html></taxonomy_single.html>
</base.html>
```

### Post page

```
<base.html>
  <blog-template.html></blog-template.html>
</base.html>
```

### 404 page

```
<base.html>
  <404.html></404.html>
</base.html>
```

## References

https://www.getzola.org/documentation/getting-started/overview/#content

https://swaits.com/adding-mermaid-js-to-zola/

https://sippo.work/blog/20231105-deploy-zola-with-cloudflare-pages/

https://zenn.dev/com4dc/scraps/c6c0f5fb87a1f9
