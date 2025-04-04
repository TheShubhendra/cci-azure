# 🚀 CircleCI Docker Executor with Azure CLI & AKS Support

This repository provides a custom Docker image for use as a **CircleCI executor**, equipped with:

- ✅ Docker CLI (for building and pushing images)
- ✅ Azure CLI (`az`) for Azure authentication
- ✅ `kubectl` for interacting with Azure Kubernetes Service (AKS)

Perfect for CI/CD pipelines that build containers and deploy to AKS via CircleCI.

---

## 📦 Image Features

- Based on `docker:dind`
- Installs:
  - Docker CLI
  - Azure CLI
  - `kubectl` (latest stable)


---

## 🛠 Usage in CircleCI

### 1. Reference the custom executor

```yaml
executors:
  azure-k8s-executor:
    docker:
      - image: TheShubhendra/circleci-aks:latest
