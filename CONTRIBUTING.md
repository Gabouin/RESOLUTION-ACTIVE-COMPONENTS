# 🤝 Contributing to TTL-Based Police Siren

Thank you for your interest in contributing to this project! Whether you want to improve the circuit design, refine the PCB layout, fix documentation, or suggest a new feature, all contributions are welcome.

---

## 📋 Table of Contents

- [What Contributions Are Welcome](#what-contributions-are-welcome)
- [How to Contribute](#how-to-contribute)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Reporting Issues](#reporting-issues)
- [Code of Conduct](#code-of-conduct)

---

## ✅ What Contributions Are Welcome

This is an electronics / PCB design project, so contributions can take many forms:

### ⚡ Circuit & Electronics
- Improvements or optimisations to the astable multivibrator circuit.
- Alternative timing values (resistors/capacitors) for different blink frequencies.
- Suggestions for additional features (e.g., sound buzzer, brightness control, power switch).

### 🖥️ PCB Design
- Layout improvements or routing optimisations.
- Alternative footprints or component choices.
- Enclosure mounting hole additions or edge-cut refinements.

### 📝 Documentation
- Fixing typos, grammar, or unclear instructions in the README or other docs.
- Adding assembly photos, renders, or step-by-step build guides.
- Translating the documentation into another language.

### 🐛 Bug Reports & Issues
- Reporting errors in the schematic or PCB layout.
- Pointing out mistakes in the BOM (wrong values, missing components, etc.).
- Suggesting improvements to the Falstad simulation or KiCad source files.

---

## 🚀 How to Contribute

### 1. Fork the repository

Click the **Fork** button at the top-right of the repository page to create your own copy.

### 2. Clone your fork

```bash
git clone https://github.com/<your-username>/TTL-SIREN.git
cd TTL-SIREN
```

### 3. Create a new branch

Use a descriptive branch name that summarises your change:

```bash
git checkout -b feat/add-buzzer
# or
git checkout -b fix/bom-capacitor-value
# or
git checkout -b docs/assembly-guide
```

### 4. Make your changes

- For **schematic or PCB changes**: Edit the KiCad project in [`Sources/KiCad`](Sources/KiCad) and export updated production files (Gerbers, BOM, etc.) to the [`production`](production) folder.
- For **documentation changes**: Edit the relevant `.md` file directly.
- For **simulation changes**: Update the Falstad link or export file in [`Sources/FALSTAD`](Sources/FALSTAD).

### 5. Commit your changes

Write a clear, concise commit message:

```bash
git add .
git commit -m "feat: add buzzer output to siren circuit"
```

### 6. Push and open a Pull Request

```bash
git push origin feat/add-buzzer
```

Then open a Pull Request on GitHub against the `main` branch and describe:
- **What** you changed.
- **Why** you changed it.
- Any **known limitations** or things still to do.

---

## 🔍 Submitting a Pull Request

To keep things consistent and easy to review, please follow these guidelines:

- Keep pull requests focused on a single topic. Separate unrelated changes into separate PRs.
- Include screenshots or renders when modifying the schematic or PCB — this makes it much easier to review.
- Update the `README.md` if your change affects the BOM, circuit description, or production files.
- Make sure file names follow the existing naming convention.

---

## 🐛 Reporting Issues

If you find a problem, please [open an issue](../../issues/new) and include:

- A clear description of the problem.
- Steps to reproduce it (e.g., "The simulation shows the LEDs do not blink at the expected frequency with the listed R/C values").
- Screenshots, measurements, or scope captures if relevant.

---

## 🌟 Sharing Your Build

Have you built this project? We'd love to see it! You can:

- Open an issue with the label **"Show and Tell"** and share your photos.
- Link to your build in the issue or in a comment.

---

## 📜 Code of Conduct

This project follows a simple rule: **be respectful and constructive**. Everyone is welcome regardless of experience level. If you are new to electronics, PCB design, or GitHub — don't hesitate to ask questions in the issues.

---

Thank you for helping make this project better! 🚀
