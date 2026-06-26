# Staging Rollback Plan

Owner confirmation for row 43 rollback evidence.

- rollback alias: `[rollback-plan-1]`
- owner: `#13`
- rule: forward-only(D7-4) plus prior-image redeploy
- trigger: failed staging approval gate, failed post-deploy smoke, failed artifact topology preflight, or owner stop decision
- rollback action: redeploy the last owner-approved image/reference through the same `staging` Environment gate
- database rule: no down migration is assumed; schema remediation remains forward-only
- evidence rule: record deployment/run alias only; do not paste env dumps, xtrace, object refs, or resolved secret material