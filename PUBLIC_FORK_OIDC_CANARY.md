# Public-fork OIDC canary

This pull request intentionally changes its own workflow permissions. The job requests repository write scopes and `id-token: write` so the Actions log can show whether GitHub downgrades repository authority for a public fork while retaining the OIDC request capability.

The workflow performs no checkout, makes no authenticated repository write, and prints only selected decoded OIDC claims.

Each update creates a fresh protected run so Kennedy's exact-SHA authorization can be exercised.
