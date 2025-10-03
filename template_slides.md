---
marp: true
theme: extra
paginate: true
html: true
footer: Template slides - Marp features demo
---

<!-- Course logo override -->
<style> section::before{ background: url("logos/uv_etse_isp.png") no-repeat center/contain; } </style>

<!-- Course font override -->
<style> section { font-family: 'Open Sans', sans-serif; } </style>

<!-- _class: small no-footer -->

![center](logos/uv_etse_isp.png)

<br>

![left w:450px](imgs/example1.jpeg)

# Template slides: Marp features demo

### Course Name

Oscar José Pellicer Valero
`Oscar.Pellicer@uv.es`

Departament d'Enginyeria Electrònica
Escola Tècnica Superior d'Enginyeria

*This template demonstrates all the features available in the `extra.css` theme*

---

<!-- _class: small -->

## Font and text styling

This slide demonstrates the various text styling options:

- **Bold text** for emphasis
- *Italic text* for highlights
- `Code snippets` for technical content
- Any ***combination `of the above`***
- Links: [Google](https://www.google.com)
- Mathematical Expressions:
  - Inline math: $P(w|h) = \frac{C(h, w)}{C(h)}$
  - Block math:
$$
P(w_1, \dots, w_n) = P(w_1)P(w_2|w_1)P(w_3|w_1, w_2)\dots P(w_n|w_1, \dots, w_{n-1})
$$
> Citations

---

## Centered images

![center w:320px](imgs/example1.jpeg)

This demonstrates centered images using the `center` attribute. You can also control the size with the `w:` parameter (or with the `h:` parameter for height): 

```markdown
![center w:400px](imgs/your-image.png)
```

---

<!-- _class: small -->

## Right and left floating images

![left sepia:50% w:300px](imgs/example1.jpeg)

This text flows around the left-aligned image. The image is positioned using the `left` attribute in the alt text, and the width is controlled with the `w:` parameter.

The text continues to wrap around the image naturally, creating a professional layout that's commonly used in academic presentations.

We can break the floating with the `clear` class:
`<div class="clear"></div>`

<div class="clear"></div>

![right sepia:90% brightness:0.8 w:200px](imgs/example1.jpeg)

Similarly, this text flows around a right-aligned image. The positioning is controlled through the alt text attributes, making it easy to create dynamic layouts without complex CSS.

Notice that this slide has the `small` class (`<!-- _class: small -->`), so the text is smaller than the default.

---

## Background images

![bg blur:10px opacity:0.6 sepia:30% brightness:0.9](imgs/example1.jpeg)

This slide demonstrates a full background image using the `bg` attribute. The image covers the entire slide background. 

You can also add effects to the background image, like `blur`, `opacity`, `sepia`, `brightness`, etc. For instance, the image in this slide has the following effects: 

```markdown
![bg blur:10px opacity:0.6 sepia:30% brightness:0.9](imgs/example1.jpeg)
```

---

<!-- _class: no-footer -->

![bg right:40% brightness:0.6](imgs/example1.jpeg)

This slide shows a background image positioned to the right with 40% width using `bg right:40%` and a brightness of 0.6: `bg right:40% brightness:0.6`

---

<!-- _class: no-footer -->

![bg left:60% sepia:50%](imgs/example1.jpeg)

This slide demonstrates a background image on the left (60% width) with a sepia filter: `bg left:60% sepia:50%`

---

## Multi-column layouts

<!-- _class: small -->

<div class="columns">
<div>

**Two-column layout**
*   First column content
*   Can contain any element

**Important notes:**
- When using any html code within the markdown file, **always** remember to leave a blank line before and after the html code, otherwise the markdown will not be rendered correctly. 
- Also remember to close all the `<div>` tags that you open, like this: `</div>`.

</div>
<div>

**Second Column**
*   Additional content here
*   Each column is equally sized

**Usage:**
```html
<div class="columns">
<div>

  Content for column 1

</div>
<div>

  Content for column 2

</div>
</div>
```

</div>
</div>

---

## Three-column layout

<div class="columns3">
<div>

**Column 1**
*   Feature A
*   Feature B
*   Feature C

</div>
<div>

**Column 2**
*   Feature D
*   Feature E
*   Feature F

</div>
<div>

**Column 3**
*   Feature G
*   Feature H
*   Feature I

</div>
</div>

---

## Figure containers with captions

<div class="figure-container align-right" style="width: 300px;">
  <img src="imgs/example1.jpeg" alt="Workflow diagram" width="300">
  <p class="figcaption">This is a right-aligned figure with a caption.</p>
</div>

This demonstrates how to create professional figures with captions. The figure container allows for precise positioning and styling of images with descriptive text.

The text flows naturally around the figure, creating a clean, academic presentation style that's perfect for technical courses.

However, the syntax is a bit verbose, so we try to avoid it if possible.

---

<!-- _class: small -->

## Code examples

### Python Code Block

```python
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.linear_model import LogisticRegression

vect = CountVectorizer()
modelLR = LogisticRegression()

# Train the model
X_train_vectorized = vect.fit_transform(X_train)
modelLR.fit(X_train_vectorized, y_train)

# Make predictions
X_test_vectorized = vect.transform(X_test)
predictions = modelLR.predict(X_test_vectorized)
```

### Inline Code

Use `CountVectorizer()` for bag-of-words representation and `TfidfVectorizer()` for TF-IDF weighting.

---

<!-- _class: small -->

## Tables and data presentation

| Algorithm | Accuracy | Precision | Recall | Anything: $\sum_1^N\frac{(y-y_{hat})^2}{N}$ |
|:----------|:---------:|:---------:|:--------:|:---------:|
| Naive Bayes | 0.85 | 0.83 | 0.87 | 0.85 |
| Logistic Regression | **0.88** | 0.86 | `0.90` | `0.88` |
| Random Forest | *0.87* | 0.85 | 0.89 | 0.87 |

A table can be created with the `|` character. Note that we use the `:` character to customize the alignment of the text in the table.

By default, tables are left-aligned within the slide. To center the table (or any other element), you can enclose it in `<div align="center"> ... </div>` tags:

<div align="center">

| Algorithm | Accuracy | Precision | Recall | Anything: $\sum_1^N\frac{(y-y_{hat})^2}{N}$ |
|:----------|:---------:|:---------:|:--------:|:---------:|
| Naive Bayes | 0.85 | 0.83 | 0.87 | 0.85 |

</div>

---

## Absolute positioning example

<div class="abs-pos" style="right: 50px; top: 50px; width: 600px; z-index: 1;">
  <img src="logos/uv_isp.png" alt="Positioned image" style="width: 100%; height: 100%; object-fit: cover;">        
</div>

This demonstrates absolute positioning capabilities. The image is positioned at specific coordinates (50px from right, 50px from top) with a defined width and height.

**Usage Notes:**
- Coordinates are relative to the slide
- Default slide size is 1280x720px
- Use z-index to control layering
- Perfect for precise positioning
- **Avoid using absolute positioning if possible**, use the other positioning methods (float, center) instead

---

## Reference and citation styling

This slide demonstrates the reference styling feature:

The reference class provides consistent styling for citations and references throughout the presentation.

<div class="reference">

[Natural Language Processing with Python](https://www.nltk.org/book/) - Bird, Klein & Loper

</div>

---

<!-- _class: no-footer -->

## Custom classes and styling

There are several classes you can use to style your slides:

- `<!-- _class: small -->`: This slide uses the `small` class to reduce font size to 24px, perfect for content-heavy slides.
- `<!-- _class: smaller -->`: This slide uses the `smaller` class for even more compact text at 20px.
- `<!-- _class: smallest -->`: This slide uses the `smallest` class for the smallest text at 18px.

Additionally, you can use the `no-footer` class to remove the footer and logos from the slide: `<!-- _class: no-footer -->`

---

## Mathematical Formulas and Equations

<div class="columns">
<div>

Bayes' Theorem:
$$ P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)} $$

Naive Bayes Classification:
$$ P(y|x_1, \dots, x_n) = \frac{P(y) \prod_{i=1}^{n} P(x_i|y)}{P(x_1, \dots, x_n)} $$

</div>
<div>

TF-IDF Formula:
$$ \text{TF-IDF}(t,d) = \text{TF}(t,d) \times \text{IDF}(t) $$

Where:
- $\text{TF}(t,d)$ is the term frequency
- $\text{IDF}(t) = \log\frac{N}{df(t)}$ is the inverse document frequency

</div>
</div>
