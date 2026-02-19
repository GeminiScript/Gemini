# Gemini Scripts

This directory contains helper scripts for working with the Gemini repository.

## Structure

- Put executable shell scripts in this folder.
- Prefer clear, task-oriented file names (for example: `setup.sh`, `build.sh`, `test.sh`).
- Add a short header comment in each script that explains purpose and usage.

## Script conventions

- Use `bash` for shell scripts unless another runtime is required.
- Start scripts with:

  ```bash
  #!/usr/bin/env bash
  set -euo pipefail
  ```

- Keep scripts idempotent where possible.
- Print actionable error messages.

## Running scripts

From the repository root:

```bash
chmod +x scripts/<script-name>.sh
./scripts/<script-name>.sh
```

## Adding new scripts

When you add a script, also update this README with:

1. Script name
2. What it does
3. Required environment variables or dependencies
4. Example command
