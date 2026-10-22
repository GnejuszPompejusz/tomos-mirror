 **tomos – Build Workflows**

This repository contains GitHub Actions workflows used to build the **Tomos** application from its main GitLab repository.

The workflows generate build artifacts for:

- **Windows**
- **Android**
- **F‑Droid**

In addition to building the app, the F‑Droid workflow also **creates an import repository** that can be used by the F‑Droid build system.

This repository does *not* contain the application source code — only the automation required to build it.

---

## **📦 Repository Structure**

```
/.github/workflows/
    windows.yml      → builds the Windows version of Tomos
    android.yml      → builds and signs the Android APK/AAB
    fdroid.yml       → builds the F‑Droid package and generates the import repo
README.md
```

---

## **🚀 Build Targets**

### **Windows**
- Builds the Windows desktop version of Tomos  
- Produces installer or binary artifacts

### **Android**
- Builds APK/AAB from the GitLab source repository  
- Signs the app using keys stored in GitHub Secrets  
- Publishes build artifacts

### **F‑Droid**
- Builds the app in a reproducible F‑Droid‑compatible environment  
- Generates metadata and the **F‑Droid import repository**  
- Produces artifacts ready for F‑Droid inclusion

```
https://gnejuszpompejusz.github.io/tomos-mirror
```
You can scan this file to add this repo to F-Droid app.

[![QR Code](https://api.qrserver.com/v1/create-qr-code/?size=220x220&data=https://gnejuszpompejusz.github.io/tomos-mirror/repo)](https://gnejuszpompejusz.github.io/tomos-mirror/repo)

---

## **🔧 Requirements**

- GitHub Actions enabled  
- Access to the main GitLab repository  
- Required secrets configured (signing keys, tokens, etc.)

---

## **📄 How It Works**

1. A push, tag, or manual trigger starts the workflow.
2. The workflow fetches the Tomos source code from GitLab.
3. The appropriate build process runs depending on the platform.
4. Artifacts are produced and stored as GitHub Actions outputs.
5. For F‑Droid, an **importable repository** is generated automatically.

---

## **🎯 Purpose**

This repository serves as a centralized CI/CD layer for building Tomos across multiple platforms, without modifying the main application repository.

