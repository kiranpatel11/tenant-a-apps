# tenant-a-apps — Tenant A applications (demo-env)

GitOps repository for **tenant-a** namespace workloads on demo-env.

Synced by the platform `ApplicationSet` in [ocp-platform](https://github.com/YOUR_GITHUB_ORG/ocp-platform) (`charts/tenant-onboarding`).

## Layout

```
deploy/
├── Chart.yaml
├── values.yaml
└── templates/
    ├── deployment.yaml
    ├── service.yaml
    └── route.yaml
```

## Local validation

```bash
helm lint deploy
helm template tenant-a deploy -f deploy/values.yaml --namespace tenant-a
```

## Ownership

- Namespace: `tenant-a`
- Argo CD AppProject: `tenant-a`
- Owner group: `tenant-a-owners`

## Related repositories

- [ocp-bootstrap](https://github.com/YOUR_GITHUB_ORG/ocp-bootstrap) — IdP and RBAC for tenant-a-owner
- [ocp-platform](https://github.com/YOUR_GITHUB_ORG/ocp-platform) — ApplicationSet entry for this repo
