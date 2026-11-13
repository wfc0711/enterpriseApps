# enterpriseApps

Application teams' repo of the KubernetesWorkloadManagement PoC (public, assumption A1).
Each app has `<app>/` with `base/` (the workload), `components/contract/` (copies the declared values into the gate Job)
and `environments/<ENV>/` per environment (`DEV`, `PROD` in the PoC): `kustomization.yaml`, `infraManifest.yaml` (what
the app team declares: EA ID, environment, release ID, custom block version, gate version) and `gate-settings.yaml`.
Each environment pulls its infra block from the `infra` repo as a remote base at a tag (`appCustomizedInfra/<app>`).
Folder names are upper case (`DEV`, `PROD`); every value in the files is lower case.

| Folder | Content |
|---|---|
| `gate-test/` | test app for the governance gate (EA-9999): `base/`, `components/contract/`, `environments/DEV/`, `environments/PROD/` |

Secrets and evidence never enter this repo (`.gitignore`).
