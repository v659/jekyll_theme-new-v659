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

<div class="editor-container">
  <textarea id="code-input" spellcheck="false">def greet():
    print("Hello!")</textarea>
  <pre class="language-python" id="highlighted-code"><code>def greet():
    print("Hello!")</code></pre>
</div>


<script>
const textarea = document.getElementById("code-input");
const highlighted = document.getElementById("highlighted-code");

function highlightCode(code) {
  // Escape HTML
  code = code
    .replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;");

  // Simple custom rules
  code = code
    .replace(/\b(def|print|return|if|else|for|while|in|import)\b/g,
             '<span class="highlighted-keyword">$1</span>')
    .replace(/(".*?"|'.*?')/g,
             '<span class="highlighted-string">$1</span>');

  return code;
}

textarea.addEventListener("input", () => {
  const code = textarea.value;
  highlighted.innerHTML = `<code>${highlightCode(code)}</code>`;
});

// Initial render
highlighted.innerHTML = `<code>${highlightCode(textarea.value)}</code>`;
</script>





---

