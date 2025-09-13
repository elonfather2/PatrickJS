<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Code Folding</title>
  <style>
    pre {
      white-space: pre-wrap; /* Wraps text inside the code block */
      margin: 0;
      padding: 10px;
      border: 1px solid #ccc;
      background: #f9f9f9;
    }
    .folded {
      display: none;
    }
    .toggle {
      cursor: pointer;
      color: blue;
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <h1>Code Folding Example</h1>
  <div>
    <span class="toggle" onclick="toggleFold(this)">[+] Show Code</span>
    <pre class="folded">
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet('World');
    </pre>
  </div>

  <script>
    function toggleFold(toggle) {
      const pre = toggle.nextElementSibling; // The <pre> element
      if (pre.classList.contains('folded')) {
        pre.classList.remove('folded');
        toggle.textContent = '[-] Hide Code';
      } else {
        pre.classList.add('folded');
        toggle.textContent = '[+] Show Code';
      }
    }
  </script>
</body>
</html>
