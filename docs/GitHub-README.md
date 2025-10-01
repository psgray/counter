# Counter App

[![Flutter CI](https://github.com/psgray/counter/actions/workflows/flutter-ci.yml/badge.svg)](https://github.com/psgray/counter/actions/workflows/flutter-ci.yml)
[![Flutter Build](https://github.com/psgray/counter/actions/workflows/flutter-build.yml/badge.svg)](https://github.com/psgray/counter/actions/workflows/flutter-build.yml)

A simple Flutter **counter app** scaffold generated with `flutter create`, enhanced with a full **CI/CD pipeline** for quality checks and multi-platform builds.

------

## 🚀 Getting Started

Clone the repo and run locally:

```
git clone https://github.com/psgray/counter.git
cd counter
flutter pub get
flutter run
```

------

## 🧪 Features

- Increment counter with a button
- State managed via `StatefulWidget`
- Ready-to-use GitHub Actions workflows (CI/CD)
- Automatic release changelogs & coverage reporting

------

## 🛠️ Development & CI/CD

This repository includes a full CI/CD pipeline using **GitHub Actions**.
Here’s how it works:

### ✅ Continuous Integration (fast checks)

- Workflow: [`.github/workflows/flutter-ci.yml`](https://chatgpt.com/c/.github/workflows/flutter-ci.yml)
- Runs on **every push and pull request**.
- Steps:
  - `flutter analyze` → static analysis
  - `dart format` → formatting check
  - `flutter test --coverage` → runs tests with coverage
  - Uploads coverage results to Codecov

⚡ These checks run quickly (≈ 2–3 minutes) and must pass before code can be merged.

------

### 🏗️ Continuous Delivery (artifact builds)

- Workflow: `.github/workflows/flutter-build.yml`
- Runs on:
  - Pushes to **main**
  - Tagged releases (e.g. `v1.0.0`)
  - Manual triggers via the Actions tab
- Builds:
  - **Android APK** (`counter-<version>-android.apk`)
  - **Windows** (`counter-<version>-windows.zip`)
  - **Linux** (`counter-<version>-linux.zip`)
  - **macOS** (`counter-<version>-macos.zip`)
  - **Web** (`counter-<version>-web.zip`)

📦 Artifacts are available in the **Actions run summary**.
For releases, they are also attached to the **GitHub Release page**.

------

### 📋 Release automation

- Workflow: `.github/workflows/release-drafter.yml`
- Automatically creates a **draft changelog** when pull requests are merged.
- Groups changes by label (Features, Fixes, Maintenance).
- When ready, you just publish the draft release.

------

### 🔒 Branch protection

- The `main` branch is protected:
  - PR required before merging.
  - All checks (`flutter-ci.yml`) must pass.
  - Linear history enforced.
- ✅ This ensures `main` always stays clean, tested, and releasable.

------

## 🧑‍💻 Contributor workflow

1. Create a feature branch → `git checkout -b feat/my-feature`
2. Commit & push → open a Pull Request
3. CI checks run automatically (lint, tests, coverage)
4. After review & approval → merge into `main`
5. On merge → full builds run, artifacts produced
6. On tagging a release → versioned artifacts published with changelog

------

## 📜 License

This project is provided under the MIT License.
