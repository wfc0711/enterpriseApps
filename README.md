# enterpriseApps

Application teams' repo of the KubernetesWorkloadManagement PoC (public, assumption A1).
Each app has `app-00x/` (later phases) with `base/`, the lanes `dev/` and `prod/` (Kustomize overlays) and `app-identity.yaml`.
Each lane pulls its infra block from the `infra` repo as a remote base at a tag (`appCustomizedInfra/<app>`).

| Folder | Content |
|---|---|
| `gate-test/` | test app for the governance gate (EA-9999), kept until Phase 1b passes: `base/`, `contract/` (copies the declared values into the gate Job), `dev/`, `prod/` |

Secrets and evidence never enter this repo (`.gitignore`).
