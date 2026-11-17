# Bachelor's Thesis: Web Architectures & Performance

[![Thesis](https://img.shields.io/badge/Degree-Bachelor's%20in%20Computer%20Science-blue.svg?style=flat-square)]()
[![University](https://img.shields.io/badge/University-Milano--Bicocca%20%28UniMiB%29-990000.svg?style=flat-square)](https://www.unimib.it/)
[![Language](https://img.shields.io/badge/Language-LaTeX%20%2F%20Italian-008080.svg?style=flat-square&logo=latex)](main.tex)
[![Status](https://img.shields.io/badge/Status-Defended%20%2F%20Graduated-success.svg?style=flat-square)]()
[![Read Online](https://img.shields.io/badge/Read%20PDF-GitHub%20Pages-brightgreen.svg?style=flat-square&logo=adobeacrobatreader)](https://ferrariochristian.github.io/tesi-triennale/main.pdf)

This repository contains the complete LaTeX source code, figures, and compiled dissertation for **Christian Ferrario**'s Bachelor's Degree Final Thesis (*Relazione della prova finale di Laurea Triennale in Informatica*) at the **University of Milano-Bicocca** (A.Y. 2023–2024).

- **Title:** *Architetture e Performance delle Applicazioni Web: Tecniche di Rendering e Gestione delle Risorse*  
  *(Architectures and Performance of Web Applications: Rendering Techniques and Resource Management)*
- **Candidate:** Christian Ferrario (ID: 886230)
- **Advisor (*Relatore*):** Prof. Sara Lucia Manzoni
- **Academic Year:** 2023–2024
- **Compiled PDF:** Available directly in the repository as [`main.pdf`](main.pdf).

---

## Abstract & Research Topics

Modern web development has evolved rapidly from static, server-rendered hypermedia documents into intricate, client-driven distributed applications. This dissertation provides an in-depth technical analysis of web rendering architectures, the runtime mechanics of the browser JavaScript engine, and the trade-offs between server execution and client hydration.

### Key Focus Areas:

1. **JavaScript Engine & Execution Internals:**
   - Architectural analysis of the Google V8 engine (Call Stack, Memory Heap, Ignition Interpreter, TurboFan Compiler).
   - The Browser Concurrency Model: Execution Contexts, Web APIs, Task Queue (Macrotasks), Microtask Queue, and Event Loop tick semantics.
   - Asynchronous execution paradigms: Promises, microtask resolution, and Event Loop starvation mitigation.

2. **Comparative Web Rendering Architectures:**
   - **Client-Side Rendering (CSR):** Single-Page Applications (SPAs), bundle size inflation, Time-to-First-Byte (TTFB) vs. First Contentful Paint (FCP) vs. Time to Interactive (TTI).
   - **Server-Side Rendering (SSR):** Full HTML generation on request, dynamic cacheability, server load trade-offs, and search engine optimization (SEO).
   - **Static Site Generation (SSG) & Incremental Static Regeneration (ISR):** Pre-rendered static assets, edge caching, and build-time scaling.

3. **The Hydration Bottleneck & Next-Gen Paradigms:**
   - The Hydration cost: DOM reconciliation, event listener attachment, duplicate execution of JavaScript on both server and client.
   - The *"Uncanny Valley"* phenomenon where UI appears rendered but remains unresponsive to user input.
   - Advanced solutions: Selective Hydration (React 18), Partial / Progressive Hydration, Island Architecture (Astro), and Resumability (Qwik).

4. **Resource Management & Web Performance Optimization:**
   - Code-splitting, dynamic imports, and route-based chunking.
   - Resource loading strategies: `async` vs `defer`, speculative prefetching (`<link rel="prefetch">`), preloading (`rel="preload"`), and DNS pre-connections.
   - Core Web Vitals optimization: Largest Contentful Paint (LCP), Interaction to Next Paint (INP), Cumulative Layout Shift (CLS).

---

## Thesis Structure

```
├── chapters/
│   ├── frontespizio.tex       # Official UniMiB frontispiece
│   ├── introduzione.tex       # Chapter 1: Introduction and historical evolution of the Web
│   ├── javascript/            # Chapter 2: JavaScript internals, V8 engine, and the Event Loop
│   ├── architectures/         # Chapter 3: CSR, SSR, SSG, and architectural trade-offs
│   ├── hydration/             # Chapter 4: Hydration mechanics, bottlenecks, and Islands/Resumability
│   └── performance/           # Chapter 5: Code-splitting, resource hints, and Core Web Vitals
├── settings/                  # Document styling, macro packages, and custom typography
├── images/                    # Architectural diagrams, execution flowcharts, and benchmarks
├── bibliografia.bib           # Comprehensive bibliography (academic papers, RFCs, W3C standards)
├── main.tex                   # Primary document entrypoint
└── main.pdf                   # Compiled, defense-ready thesis dissertation
```

---

## Compiling the Dissertation

To compile the LaTeX document from source, ensure you have a complete TeX Live or MacTeX installation with `biber` for bibliography generation:

```bash
# 1. Compile document structure
pdflatex main.tex

# 2. Process citations and bibliography
biber main

# 3. Final cross-reference resolution
pdflatex main.tex
pdflatex main.tex
```

Or automate the full build pipeline via `latexmk`:
```bash
latexmk -pdf main.tex
```

---

## Status & Disclaimer

> [!NOTE]
> **Academic Thesis — Defended & Completed.**
> Officially submitted and defended for the Bachelor of Science in Computer Science at the University of Milano-Bicocca. Preserved for academic citation and portfolio reference.

---

## License

The textual content, diagrams, and dissertation materials are protected by copyright © Christian Ferrario, Università degli Studi di Milano-Bicocca.
