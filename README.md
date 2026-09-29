# Engineering Mechanics — Interactive Exam Preparation

An interactive GitHub Pages learning tool designed to help students revise core Engineering Mechanics concepts through **concept review, guided MCQ practice, weak-area revision, and exam-style tests**.

The project is intentionally lightweight: it runs entirely in the browser using a single `index.html` file and does **not** require a backend, database, login, or installation.

---

## 🎯 Purpose

The page is designed to help students move through a simple learning cycle:

**Learn → Practice → Identify Weak Areas → Test Yourself**

Instead of using MCQs only for scoring, the page uses them as a learning tool. Practice questions provide progressive hints and explanations, while Exam Mode removes hints and delays feedback until the end.

---

## 📚 Syllabus Coverage

The current version contains **110 MCQs** organised into six modules:

### Module 1 — Distributed Loads & Rigid-Body Equilibrium
- Distributed loading
- Equivalent resultant force
- Location of resultant
- Free-body diagrams
- Support reactions
- Conditions of rigid-body equilibrium
- 2D equilibrium
- 3D equilibrium
- Constraints
- Static determinacy and indeterminacy

### Module 2 — Internal Forces, Shear & Moment
- Internal normal force
- Internal shear force
- Bending moment
- Shear-force diagrams
- Bending-moment diagrams
- Load–shear relationship
- Shear–moment relationship
- Area relationships between load, shear, and moment

### Module 3 — Trusses, Frames & Machines
- Simple planar trusses
- Two-force members
- Method of joints
- Zero-force members
- Method of sections
- Tension and compression
- Frames
- Machines
- Internal pin forces

### Module 4 — Centroid, Center of Gravity & Composite Bodies
- First moment of area
- Center of gravity
- Center of mass
- Centroid
- Symmetry
- Composite areas
- Composite bodies
- Treatment of holes as negative areas

### Module 5 — Area Moments of Inertia
- Definition of area moment of inertia
- Parallel-axis theorem
- Radius of gyration
- Composite areas
- Product of inertia
- Symmetry and product of inertia

### Module 6 — Mass Moment of Inertia
- Definition of mass moment of inertia
- Parallel-axis theorem
- Radius of gyration
- Composite bodies
- Difference between area and mass moments of inertia

---

## ✨ Features

### 📘 Learn Mode
Each module contains concise concept cards with:
- important definitions,
- governing equations,
- common conceptual distinctions,
- key reminders before attempting MCQs.

### 🧠 Practice Mode
Practice mode includes:
- shuffled questions,
- shuffled answer choices,
- immediate feedback,
- progressive hints,
- explanations,
- key takeaways,
- first-attempt tracking.

### 🔥 Weak-Area Revision
The page stores learning progress in the browser and identifies topics with low mastery.

Questions answered incorrectly are saved for targeted revision.

### ⏱ Exam Mode
Exam Mode provides:
- mixed-syllabus tests,
- 15-question and 25-question options,
- no hints during the test,
- no correctness feedback until submission,
- score, accuracy, and review after completion.

### 📐 Visual Questions
The question bank includes original diagrams for topics such as:
- distributed loading,
- support reactions,
- free-body diagrams,
- beams,
- shear/moment interpretation,
- trusses,
- zero-force members,
- method of sections,
- centroids,
- composite areas,
- moments of inertia.

### 📊 Mastery Tracking
Progress is stored using browser `localStorage`.

The page tracks:
- total questions answered,
- first-attempt accuracy,
- module mastery,
- weak topics,
- previously missed questions.

No student data is uploaded anywhere.

---

## 📊 Current Question Distribution

| Module | Questions |
|---|---:|
| Distributed Loads & Rigid-Body Equilibrium | 24 |
| Internal Forces, Shear & Moment | 20 |
| Trusses, Frames & Machines | 20 |
| Centroid, Center of Gravity & Composite Bodies | 16 |
| Area Moments & Product of Inertia | 18 |
| Mass Moment of Inertia | 12 |
| **Total** | **110** |

---

## 🚀 Running the Page Locally

The simplest method is to open:

```text
index.html
```

directly in a modern browser.

For the best experience, especially if additional files are added later, run a simple local server.

Using Python:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 🌐 Publishing with GitHub Pages

### 1. Create or open a GitHub repository

For example:

```text
engineering-mechanics
```

### 2. Upload the page

Make sure the main file is named exactly:

```text
index.html
```

and is located in the root of the repository.

### 3. Enable GitHub Pages

Open:

**Repository → Settings → Pages**

Under **Build and deployment**, select:

```text
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

Click **Save**.

### 4. Open the published site

The page will normally be available at:

```text
https://YOUR-USERNAME.github.io/engineering-mechanics/
```

If the repository is named:

```text
YOUR-USERNAME.github.io
```

then the site URL is:

```text
https://YOUR-USERNAME.github.io/
```

---

## 🔄 Updating the Website

To publish a newer version:

1. Replace the existing `index.html`.
2. Commit the updated file to the `main` branch.
3. Wait briefly for GitHub Pages to redeploy.
4. Refresh the published page.

If the old version still appears, perform a hard refresh:

**macOS**

```text
Command + Shift + R
```

**Windows/Linux**

```text
Ctrl + Shift + R
```

---

## 🗂 Recommended Repository Structure

The current version works with only one file:

```text
engineering-mechanics/
│
├── index.html
└── README.md
```

A future modular version can use:

```text
engineering-mechanics/
│
├── index.html
├── README.md
├── css/
│   └── style.css
├── js/
│   ├── app.js
│   ├── quiz.js
│   └── storage.js
├── questions/
│   ├── equilibrium.js
│   ├── beams.js
│   ├── trusses.js
│   ├── centroids.js
│   ├── area-inertia.js
│   └── mass-inertia.js
└── assets/
    └── diagrams/
```

The single-file version is easier to deploy and maintain, while the modular structure is better if the question bank grows substantially.

---

## 🧮 Mathematics Rendering

The page uses **MathJax** to render equations such as:

```text
ΣFx = 0
ΣFy = 0
ΣM = 0
```

and

```text
dV/dx = w(x)
dM/dx = V(x)
```

An internet connection is required for MathJax to load from its CDN unless a local copy is added later.

---

## 💾 Progress Storage

Student progress is stored locally in the browser using:

```javascript
localStorage
```

This means:
- no account is required,
- no server is required,
- progress remains on that browser/device,
- clearing browser storage will reset saved progress.

The page also includes a **Reset Progress** option.

---

## 🧑‍🏫 Suggested Student Workflow

For best results:

1. Read the concept cards in **Learn**.
2. Attempt the related questions in **Practice**.
3. Try to answer before using hints.
4. Review the explanation after each mistake.
5. Use **Weak Areas** for targeted revision.
6. Attempt **Exam Mode** without notes.
7. Return to weak topics and repeat.

The objective is not simply to obtain a high score, but to reduce dependence on hints and improve first-attempt accuracy.

---

## 🛠 Planned Improvements

Possible future additions include:
- more numerical MCQs,
- additional diagram-based questions,
- complete beam SFD/BMD visual problems,
- richer truss-force questions,
- calculation-based centroid problems,
- parallel-axis theorem numericals,
- question difficulty levels,
- timed exam settings,
- topic-wise exam generation,
- downloadable performance report,
- dark mode,
- instructor-editable question bank.

---

## 👨‍🏫 Course Use

Created as an interactive revision resource for an undergraduate Engineering Mechanics course.

The material is intended for educational practice and exam preparation.

---

## 📄 License

This repository may be used and adapted for educational purposes.

If redistributed or modified, please preserve appropriate attribution to the original course-page author.
