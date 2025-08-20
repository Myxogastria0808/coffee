# coffee

**coffee** is a blog template for zola!

This template can be used **mermaid** and **katex**.

<div align="center">
  <img src="https://github.com/Myxogastria0808/coffee/blob/main/assets/coffee.webp" width="300px" height="300px" />
</div>

## Setup Environment

1. Install zola

Please install zola by referring to the following.

https://www.getzola.org/documentation/getting-started/installation/

2. Setup coffee theme

```sh
zola init < your blog project >
cd ./< your blog project >/themes/
# clone coffee theme to theme directory
git clone https://github.com/Myxogastria0808/coffee.git
cd ..
# build your blog to apply this theme
zola build
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

<!-- TODO -->

- markdown example

https://github.com/Myxogastria0808/coffee/blob/main/content/sample/index.md

- preview URL



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

<!-- TODO -->

- markdown example

https://github.com/Myxogastria0808/coffee/blob/main/content/sample/index.md

- preview URL



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
