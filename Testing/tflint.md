# 🧹 TFLint – Terraform Linter

> **TFLint** is a pluggable linter for Terraform, helping you catch common issues, enforce style consistency, and avoid cloud-specific mistakes before they reach production.

---

## 🔗 Official Resources

- [TFLint Website](https://github.com/terraform-linters/tflint)

- 📖 [Spacelifts Blog post →](https://spacelift.io/blog/what-is-tflint) 

---

## ✅ Why Use TFLint?

- Catches **syntax errors** and **deprecated features**
- Detects **cloud-specific mistakes** (e.g., wrong instance types, deprecated AMIs)
- Enforces **custom rules** and **naming conventions**
- Integrates easily with **CI/CD pipelines**
- Supports **plugin extensions** for AWS, Azure, GCP, and more

---

## ⚙️ Installation

### Option 1: Homebrew (macOS/Linux)

```bash
brew install tflint
```
### Option 2: Choco (Windows)

```bash
choco install tflint
```

## ⚙️ Use in CI/CD

### GitHub Actions Example

```bash
- name: Run TFLint
  uses: terraform-linters/setup-tflint@v4
  with:
    tflint_version: latest

- run: |
    tflint --init
    tflint

```

## My Take

I’ve found tflint especially useful for catching provider-specific errors early, enforcing naming conventions, and reducing feedback loops in PR reviews. It’s become a standard part of my Terraform workflow — especially when paired with tfsec and terraform fmt.