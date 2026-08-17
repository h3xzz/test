# Test Repository

This repository is a small example project used to demonstrate a guarded GitHub Actions e2e flow and document the trusted script that should run from the default branch.

## Overview

The workflow in `.github/workflows/e2e-replica.yml` mirrors a real-world security pattern where pull requests from forks are checked carefully before a privileged job is allowed to run. The repository contains a minimal script that is intended to represent the approved e2e test entry point.

## Repository layout

- `.github/workflows/e2e-replica.yml` — workflow definition for the e2e guard test.
- `hack/e2e-test.sh` — trusted script executed by the workflow.
- `doc` — project documentation notes.

## Local usage

```bash
chmod +x ./hack/e2e-test.sh
./hack/e2e-test.sh default-setup
```

## Notes

This project is intentionally lightweight and is primarily intended as a documentation and test fixture rather than a full application.
