
# Bulls & Cows Web Solver

A pure‑front‑end implementation that helps you solve the classic four‑digit **“Bulls & Cows”** (a.k.a. Mastermind with digits) puzzle.

---

## Features
| | |
|---|---|
|  **Runs entirely in the browser** – just open `index.html` locally (via a tiny HTTP server) or deploy to GitHub Pages. |
|  **Decision‑tree engine** rebuilt from the original C++ logic; guarantees the optimal next guess according to the pre‑computed `answer.all`. |
|  **Verbose log** – shows guess count (`Guess 1`, `Guess 2`…), solver’s proposal, and the feedback you type (`xAyB`). |
|  **Zero dependencies** – plain HTML + native JavaScript + CSS only. |
|  **Ready‑to‑use GitHub Actions** – CI workflow auto‑publishes the site to Pages. |

---

## Quick Start

### Local preview
```bash
git clone <your-repo>
cd <repo>
# launch a lightweight HTTP server (Python 3.x)
python -m http.server 8080
# now visit http://localhost:8080
````

> Opening the file via `file://` will fail to fetch **answer.all** because of browser security policy.

### Deploy to GitHub Pages

1. Push the entire repo (including `.github/workflows/deploy.yml`) to the **`main`** branch.
2. In **Settings → Pages**, choose **Source: GitHub Actions**.
3. Re‑run the workflow or push a new commit – the site will be available at
   `https://<username>.github.io/<repo>/`.

---

## How to Play

1. The page loads and prints the **first guess**, e.g. `Guess 1: 0123`.
2. Type your feedback in the form `xAyB` (e.g. `1A2B`) and press **Enter**.
3. The log records

   * `Feedback: 1A2B` (your input)
   * `Guess 2: 0245` (solver’s next move)
4. Repeat until the solver announces **“Correct! The answer is XXXX”.**

---



## Customization

* **Dark mode / Themes** – tweak CSS variables in the `<style>` block.
* **New decision tree** – regenerate `answer.all` with your C++ tool and replace the file.
* **Internationalization** – edit static strings in `index.html` or swap in `README_zh.md` for Chinese docs.

---


