# PDK / Technology Library Setup

This repository does **not** include the 180nm foundry PDK files — they're
proprietary/licensed and are excluded via `.gitignore`. Anyone cloning this
repo needs to obtain the PDK separately (through your university/foundry
license agreement) and link it into the workspace locally.

## What's excluded

See the "180nm technology / PDK files" section in [`.gitignore`](../.gitignore).
It covers common ADS PDK folder-naming patterns. If your specific PDK folder
doesn't match, add its exact name to `.gitignore` before your first commit —
check `git status` to confirm it isn't showing up as a new/untracked file
before you `git add .`.

## Setting up the PDK locally (after cloning)

1. Obtain the 180nm PDK through your institution's licensing channel.
2. Place/link it inside `ads_workspace/<your_workspace>_wrk/` following your
   PDK provider's ADS integration instructions (usually via
   `Technology > Import/Manage Libraries` in ADS, or by editing the
   workspace's library definition file to point at your local PDK install).
3. Re-open the workspace in ADS and verify the technology libraries resolve
   (no missing-library warnings on schematic open).

## Before your first commit — sanity check

```bash
git status
```

Confirm no PDK files appear as untracked/staged. If they do, either:
- add the missing folder/file pattern to `.gitignore`, or
- explicitly `git rm --cached <path>` if already staged.
