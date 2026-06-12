# PLAIN — Plain Language Programming

<div align="center">
  <h3>A programming language that reads like plain English.</h3>
  <p>No brackets. No semicolons. No cryptic symbols. Just sentences.</p>
  <img src="https://img.shields.io/badge/version-1.0.0-7c6ff7?style=for-the-badge" alt="version" />
  <img src="https://img.shields.io/badge/license-MIT-4ade80?style=for-the-badge" alt="license" />
  <img src="https://img.shields.io/badge/made%20by-Parth%20Bhosale-f472b6?style=for-the-badge" alt="author" />
</div>

---

## ✨ Try it Online

**[→ Open the PLAIN Playground](playground/index.html)** (open `playground/index.html` in your browser)

---

## 📦 Install the CLI

```bash
npm install -g plain-lang
```

## 🚀 Quick Start

Create a file called `hello.plain`:

```plain
set name to "World"
say "Hello, " + name + "!"
```

Run it:
```bash
plain hello.plain
```

Or start the interactive REPL:
```bash
plain
```

---

## 📖 Language Reference

### Variables
```plain
set name to "Parth"
set age to 19
set price to 299.99
```

### Output & Input
```plain
say "Hello, world!"
say "Value: " + myVar
ask "What is your name?" and store in username
say "Hi, " + username
```

### Math
```plain
set result to 10 + 5 * 2
set area to width * height
set power to 2 ^ 10         -- 1024
set remainder to 17 % 5     -- 2
calculate 3.14 * r ^ 2 and store in circle_area
```

### Conditions
```plain
if score >= 90 then
  say "Grade A"
otherwise if score >= 75 then
  say "Grade B"
otherwise
  say "Try again"
end
```

Operators: `=` `!=` `>` `<` `>=` `<=` `and` `or` `not`

### Loops
```plain
-- Repeat N times
repeat 5 times
  say "Hello!"
end

-- Counted loop
count from 1 to 10 as i
  say i
end

-- Loop over a list
for each item in myList
  say item
end
```

### Lists
```plain
create list fruits
add "apple" to fruits
add "mango" to fruits
say count of fruits          -- 2
say item 1 in fruits         -- apple
```

### Functions
```plain
define step greet with name
  say "Hello, " + name + "!"
end step

define step add with a, b
  give back a + b
end step

run step greet with "Parth"
set total to run step add with 10, 20
say total
```

### Data Tables
```plain
create table students
set headers of students to "Name", "Score", "Grade"
add row "Parth", 95, "A" to students
add row "Vedant", 82, "B" to students
show table students
```

### Web Requests
```plain
fetch "https://api.example.com/data" and store in response
say response
```

### Other
```plain
wait 2          -- pause 2 seconds
stop            -- exit program
-- comment      -- this is a comment
```

---

## 🗂️ Project Structure

```
plain-lang/
├── playground/          # Browser-based IDE & landing page
│   ├── index.html       # Landing page + playground app
│   ├── style.css        # All styles
│   ├── interpreter.js   # Browser build of interpreter
│   └── app.js           # Playground UI logic
├── src/
│   ├── interpreter.js   # Core language runtime
│   └── cli.js           # CLI entry point (plain command)
├── examples/
│   ├── hello.plain
│   ├── calculator.plain
│   └── grades.plain
├── package.json
└── README.md
```

---

## 🌐 Publishing

### npm
```bash
npm login
npm publish
```

### GitHub Pages (playground)
Push the `playground/` folder to a `gh-pages` branch:
```bash
git subtree push --prefix playground origin gh-pages
```

### Vercel / Netlify
Set the root directory to `playground/` and deploy.

---

## 💡 Roadmap

- [ ] Syntax highlighting VS Code extension
- [ ] File I/O (`read file`, `write file`)
- [ ] String manipulation (`length of`, `upper`, `lower`)
- [ ] Type checking (`is number`, `is text`)
- [ ] Multi-file imports
- [ ] WASM build for faster browser execution

---

## 🧑‍💻 Author

Made with ❤️ by **Parth Pradip Bhosale**

---

## 📄 License

MIT — free to use, share, and modify.
