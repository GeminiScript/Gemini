# Gemini Scripts

This directory contains helper scripts for working with the Gemini repository.

## Structure

- Put executable scripts in this folder.
- Prefer clear, task-oriented file names (for example: `setup.sh`, `build.sh`, `test.ps1`).
- Add a short header comment in each script that explains purpose and usage.

## Script conventions

### Bash (`.sh`)

- Use `bash` unless another runtime is required.
- Start scripts with:

  ```bash
  #!/usr/bin/env bash
  set -euo pipefail
  ```

### PowerShell (`.ps1`)

- Use `pwsh` (PowerShell 7+) for cross-platform scripts.
- Start scripts with:

  ```powershell
  #Requires -Version 7.0
  Set-StrictMode -Version Latest
  $ErrorActionPreference = 'Stop'
  ```

### General

- Keep scripts idempotent where possible.
- Print actionable error messages.

## Running scripts

From the repository root:

```bash
chmod +x scripts/<script-name>.sh
./scripts/<script-name>.sh
```

```bash
pwsh -File scripts/<script-name>.ps1
```

## Adding new scripts

When you add a script, also update this README with:

1. Script name
2. Runtime (`bash`, `pwsh`, etc.)
3. What it does
4. Required environment variables or dependencies
5. Example command
