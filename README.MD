repo-root/
├── applications/
│   ├── mariadb/
│   │   ├── customer-a/
│   │   │   ├── operator.yaml             # ArgoCD app (Helm) to install operator
│   │   │   ├── instance/
│   │   │   │   ├── mariadb.yaml          # MariaDB CR for customer-a
│   │   │   │   └── kustomization.yaml
│   │   ├── customer-b/
│   │   │   ├── operator.yaml
│   │   │   ├── instance/
│   │   │   │   ├── mariadb.yaml
│   │   │   │   └── kustomization.yaml
├── environments/
│   └── dev/
│       ├── mariadb-app-of-apps.yaml      # Optional: App of Apps to include all customers

