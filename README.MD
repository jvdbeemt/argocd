repo-root/
├── applications/
│   └── mariadb/
│       ├── customer-a/
│       │   ├── namespace/
│       │   │   ├── kustomization.yaml
│       │   │   └── namespace.yaml
│       │   ├── namespace-app.yaml         # ArgoCD App: creates namespace
│       │   ├── operator.yaml              # ArgoCD App: installs MariaDB Operator (Helm)
│       │   ├── instance/
│       │   │   ├── mariadb.yaml           # MariaDB CR (custom resource)
│       │   │   └── kustomization.yaml
│       │   └── instance-app.yaml          # ArgoCD App: applies the MariaDB CR
│       │
│       ├── customer-b/
│       │   ├── namespace/
│       │   │   ├── kustomization.yaml
│       │   │   └── namespace.yaml
│       │   ├── namespace-app.yaml
│       │   ├── operator.yaml
│       │   ├── instance/
│       │   │   ├── mariadb.yaml
│       │   │   └── kustomization.yaml
│       │   └── instance-app.yaml
│
├── environments/
│   └── dev/
│       └── mariadb-app-of-apps.yaml      # App of Apps: manages all customers

