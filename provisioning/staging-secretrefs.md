# Staging Provisioning Inventory

Identifier-only provisioning evidence for row 43. Values are intentionally
omitted and must remain behind SecretRef/SecretStore boundaries.

- provisioning alias: `[secretref-inventory-1]`
- SecretStore alias: `[vault-staging-1]`
- SecretStore backend: Vault KV v2
- Vault mount: `secret/`
- staging base path: `secret/data/rpa/staging/<runtime>/<purpose>/<name>`
- identity matrix: D8-A12

## SecretRef Inventory

- `rpa/staging/runtime-worker/resume_token_hmac/active`
- `rpa/staging/runtime-worker/browser_session/active`
- `rpa/staging/artifact-lifecycle/object_store/s3`
- `rpa/staging/api/browser_session/active`
- `rpa/staging/api/signed_command/registry`

## Identity Map

- `[runtime-worker-1]`: runtime-worker purpose refs only
- `[browser-worker-1]`: browser-worker purpose refs only
- `[artifact-lifecycle-1]`: artifact-lifecycle object_store refs only
- `[llm-gateway-1]`: provider alias boundary only; raw provider/model values omitted

No plaintext role_id, secret_id, Vault token, cloud key, provider key, raw model
identifier, object reference, env dump, or xtrace output belongs in this repo.