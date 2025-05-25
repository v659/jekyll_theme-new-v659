---
layout: default
title: Home
---



# Welcome to Neon-X

Neon-X is a custom orange-blue Jekyll theme with neon-ish colours

---

## Navbar

<div class="floating-navbar">
  <a href="https://v659.github.io/jekyll_theme-new-v659/">Home</a>
  <a href="https://github.com/v659/jekyll_theme-new-v659">Git</a>
  <a href="https://tonic.hackclub.com/">#Tonic</a>
</div>

---

## Highlight Box

<div class="highlight-box">
   This is a styled highlight box, useful for messages, alerts, or special notes.
</div>

---

## Underlined Text

<p class="underline-primary">This is an example of primary-colored underlined text.</p>
<p class="underline-secondary">This is an example of secondary-colored underlined text.</p>

---
## Highlighting text

<mark>This is highlighted text</mark>

---
## Headings

---

<h1>H1</h1>
<h2>H2</h2>
<h3>H3</h3>
<h4>H4</h4>
<h5>H5</h5>
<h6>H6</h6>

---

##  Typing Input

<div class="card">
  <p>Enter your name below:</p>
  <input type="text" class="typing-box" placeholder="Your name..." />
</div>

# This is a custom heading colour

<div class="card">
  <h2>Styled Buttons</h2>
  <button class="btn-primary">Primary Action</button>
  <button class="btn-secondary">Secondary Action</button>
</div>

---

## Try Typing Python Below

<div class="code-editor-container">
  <textarea id="code-input" spellcheck="false" placeholder="Type Python code here...">def greet():
    print("Hello from a neon-themed Jekyll site!")</textarea>
  <pre id="highlighted-code" aria-hidden="true"></pre>
</div>

<script>
  const textarea = document.getElementById("code-input");
  const highlighted = document.getElementById("highlighted-code");

  function escapeHtml(text) {
    return text
      .replace(/&/g, "&amp;")
      .replace(/</g, "&lt;")
      .replace(/>/g, "&gt;");
  }

  function highlightCode(code) {
    let escaped = escapeHtml(code);

    // Highlight Python keywords
    escaped = escaped.replace(
      /\b(def|print|return|if|else|elif|for|while|in|import|from|as|with|class|try|except|finally|raise|pass|continue|break|and|or|not|is|None|True|False)\b/g,
      '<span class="highlighted-keyword">$1</span>'
    );

    // Highlight strings
    escaped = escaped.replace(
      /(".*?"|'.*?')/g,
      '<span class="highlighted-string">$1</span>'
    );

    // Highlight comments
    escaped = escaped.replace(
      /(#.*?$)/gm,
      '<span class="highlighted-comment">$1</span>'
    );

    return escaped;
  }

  function updateHighlighting() {
    const code = textarea.value;
    highlighted.innerHTML = highlightCode(code);
    highlighted.scrollTop = textarea.scrollTop;
    highlighted.scrollLeft = textarea.scrollLeft;
  }

  textarea.addEventListener("input", updateHighlighting);
  textarea.addEventListener("scroll", updateHighlighting);
  updateHighlighting();
</script>







---

