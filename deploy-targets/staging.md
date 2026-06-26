# Staging Deploy Target

This repository is the external platform/deploy evidence repository for
`xorrbss/RPA-Enterprise` row 43 staging governance.

- platform repo: `xorrbss/rpa-platform-deploy`
- GitHub Environment: `staging`
- deploy target alias: `[deploy-target-gh-actions-staging-1]`
- concrete target: GitHub Actions workflow `.github/workflows/staging-approval.yml`, job `approval`, environment `staging`
- branch policy: protected `main` only through the Environment deployment branch policy
- secret material: omitted; only SecretRef and backend aliases may appear in this repo

This target is an approval/provisioning evidence gate. It does not store raw
Vault AppRole material, cloud keys, provider keys, object refs, or env dumps.