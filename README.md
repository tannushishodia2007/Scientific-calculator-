# Scientific Calculator

A browser-based scientific calculator built with plain HTML, CSS and JavaScript. It solves expressions using its own parser (tokenizer, Shunting-yard algorithm and stack evaluation) and does not use `eval()`.

**Live demo:** https://tannushishodia2007.github.io/scientific-calculator/

## Features

- Basic operations: add, subtract, multiply, divide, percent
- Scientific functions: sin, cos, tan, ln, log, square root, square, power, factorial, reciprocal
- Inverse functions (sin⁻¹, cos⁻¹, tan⁻¹, eˣ, 10ˣ) using the INV button
- Constants: π, e and the previous answer (Ans)
- Degree and radian mode
- Memory keys: MC, MR, M+, M−
- Live answer preview while typing
- Brackets close automatically
- Calculation history saved in the browser, tap any past result to reuse it
- Keyboard support
- Clear error messages (syntax error, math error, cannot divide by 0)
- Works on mobile and desktop

## How it works

1. **Tokenizer:** the typed text is split into numbers, operators, functions and brackets. Implicit multiplication such as `2π` or `3(4+5)` is handled here.
2. **Shunting-yard algorithm:** the tokens are converted from infix to postfix form using operator precedence and associativity. For example, `2+3×4` becomes `2 3 4 × +`. This is how BODMAS is followed.
3. **Stack evaluation:** the postfix list is solved from left to right using a stack.

## Example calculations

| Input | Result |
| --- | --- |
| `2+3×4` | 14 |
| `(2+3)×4` | 20 |
| `2^3^2` | 512 |
| `−2^2` | −4 |
| `sin(30)` (DEG mode) | 0.5 |
| `5!` | 120 |
| `√(144)` | 12 |
| `1÷0` | Cannot divide by 0 |

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `0-9` and `.` | Enter numbers |
| `+ - * / ^` | Operators |
| `( )` | Brackets |
| `!` and `%` | Factorial and percent |
| `Enter` or `=` | Calculate |
| `Backspace` | Delete last entry |
| `Esc` | Clear all |

## Tech stack

- HTML5
- CSS3
- JavaScript (no libraries or frameworks)

## Run locally

1. Download or clone this repository.
2. Open `index.html` in any modern browser.

No installation or build step is needed.

## Project structure

```
scientific-calculator/
├── index.html   # markup, styles and JavaScript in one file
└── README.md
```
