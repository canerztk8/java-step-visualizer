# Java Step Visualizer

A browser-based, step-by-step Java execution visualizer inspired by [MOOC.fi](https://www.mooc.fi/en/) and [PythonTutor](https://pythontutor.com/).
No installation needed — just open the HTML file in any browser.

---

## What It Does

Helps beginners understand two of Java's most confusing concepts:

- **Compile-Time Overload Resolution** — How the compiler picks a method based on *static type*
- **Runtime Dynamic Dispatch** — How the JVM finds the actual method body at runtime based on *dynamic type*

---

## Features

- Write any Java code with your own classes and inheritance
- Step through execution line by line (Prev / Next buttons or arrow keys)
- Blue arrow: current call site | Green arrow: method body execution jumped into
- Compile-Time analysis: candidates, selected signature, widening (int to double)
- Runtime analysis: class hierarchy, override detection, actual method executed
- Live Stack + Heap memory panel at every step
- Plain-language explanation box at each step
- Console output accumulates line by line

---

## Files

- `java-visualizer.html`    — Turkish interface
- `java-visualizer-en.html` — English interface

---

## Usage

**Local:** Download either .html file and double-click to open in any browser.

**Online (GitHub Pages):**
`
https://<your-username>.github.io/java-step-visualizer/java-visualizer-en.html
`

---

## Built-in Examples

- **Ober / Unter** — Classic overloading + widening + dynamic binding
- **Animal / Dog / GoldenRetriever** — 3-level inheritance with overriding
- **Shape / Circle / ColoredCircle** — Multiple overloads + multi-level override

---

## Technical Details

- No dependencies — Pure HTML + CSS + vanilla JavaScript
- No build step — single file, works offline
- Parser: regex-based Java subset parser
- Type system: full primitive widening chain (byte to short to int to long to float to double)
- Overload resolution: most-specific method selection with widening cost sorting
- Dynamic dispatch: virtual method table simulation via class hierarchy walk

---

## License

MIT — free to use, modify, and share.
