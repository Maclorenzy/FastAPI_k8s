Auteur: Laurent Hoarau

# ⚙️ FastAPI — Kubernetes Manifests

> Dépôt de manifests Kubernetes pour le déploiement et l'orchestration de l'API FastAPI Traefik.

---

## 📁 Structure du dépôt

```
📦 FastAPI_app/
├── 📂 deployments/       # Déploiements Kubernetes
├── 📂 services/          # Services & exposition des pods
├── 📂 ingress/           # Règles d'entrée (Ingress)
├── 📂 configmaps/        # Variables de configuration
├── 📂 secrets/           # Secrets (encodés base64)
└── 📂 namespaces/        # Définitions des namespaces
```

---

## 🚀 Déploiement rapide

### Prérequis

- `kubectl` configuré et connecté au cluster
- Accès au namespace cible

### Appliquer tous les manifests

```bash
kubectl apply -f .
```

### Appliquer un dossier spécifique

```bash
kubectl apply -f deployments/
kubectl apply -f services/
kubectl apply -f ingress/
```

---

## 🔍 Vérifier le déploiement

```bash
# Lister les pods
kubectl get pods

# Lister les services
kubectl get svc

# Voir les logs d'un pod
kubectl logs -f <nom-du-pod>

# Décrire un déploiement
kubectl describe deployment <nom-du-deployment>
```

---

## 🧹 Supprimer les ressources

```bash
kubectl delete -f .
```

---

## 🛠️ Stack technique

| Outil | Rôle |
|---|---|
| **FastAPI** | Framework API Python |
| **Kubernetes** | Orchestration des conteneurs |
| **Docker** | Conteneurisation |

---

## 👤 Auteur

**Maclorenzy** — [@Maclorenzy](https://github.com/Maclorenzy)

---

> 💡 *Pour toute modification, crée une branche dédiée et ouvre une Pull Request.*
