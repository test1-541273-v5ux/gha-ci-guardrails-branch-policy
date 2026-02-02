# CI Guardrails - Branch Policy

CI Guardrails - Branch Policy handles branch compliance with push event and delivers policy compliance summary as status check.

## Inputs

- `message` (optional): Message printed by the action.

## Usage

```yaml
name: ci-guardrails-branch-policy
on:
  workflow_dispatch:

jobs:
  run:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: test1-541273-v5ux/gha-ci-guardrails-branch-policy@v1
        with:
          message: "Hello from CI Guardrails - Branch Policy"
```

## Development

- `pnpm build` to compile TypeScript sources
- `pnpm test` to run unit tests


## Analytics Events Module

- Includes `src/analytics.ts` with an opt-in event emitter stub.
- Keep analytics disabled by default unless users explicitly opt in.

## Storage Module

- Includes `src/storage.ts` for lightweight state persistence.
- Example usage is wired into `src/index.ts` run counters.