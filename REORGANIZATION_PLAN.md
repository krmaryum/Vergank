# Vergank Repository — Safe Organization Plan

## Current verified root (17 November 2026)

- `AZ-104/`
- `VMware/`
- `Wintel/Day 01 Wintel Enterprise Administration, Introduction & Microsoft Fundamentals/`
- `.gitignore`

The internal contents of these folders were **not** accessible during this review. No files have been moved, renamed, or removed.

## Phase 1 — Recommended now

1. Add `README.md` to repository root.
2. Verify Git status and back up the current branch.
3. Create an optional new day folder only when you have a new class to upload.
4. Keep existing Wintel Day 01 long-name folder intact for the moment.

## Phase 2 — After folder content inventory

1. Record current paths: `git ls-files > FILE_INVENTORY.txt` (do not commit the inventory if it reveals sensitive paths).
2. Identify relative Markdown/image links before renaming folders.
3. Review duplicate files, old archives, large installers, and screenshot privacy.
4. Make a move map (`old path -> new path`) and review it before executing moves.
5. Use `git mv` only for approved moves, fixing affected relative links.
6. Check changes with `git diff --stat`, `git status`, and Markdown link checks.
7. Commit/push after verifying links on GitHub.

## Safe PowerShell commands (run inside local repo)

```powershell
cd C:\Linux\Vergank  # change if your local clone is elsewhere
git status
git pull --ff-only origin main
Copy-Item README.md README.backup.md -ErrorAction SilentlyContinue  # only if an existing README is present
# Copy the downloaded README.md to this repo root, then:
git add README.md
git diff --cached -- README.md
git commit -m "docs: add learning portfolio README"
git push origin main
```

**Do not run `git mv` until existing contents and links have been checked.**

## Folder organization policy

- Course roots remain `AZ-104/`, `VMware/`, `Wintel/`.
- New lessons: `Day-XX-Short-Topic/` under the corresponding course.
- Detailed notes in `English/` and `Roman_Urdu/`.
- Keep original transcripts in `Source_Transcript/` only if you have permission to publish them and they contain no private student or instructor information.
- Save verified notes in `Technical_Verification/` rather than overwriting lecture text.
- Keep screenshots sanitized and documented.

## Next audit step

Run `git ls-files` from the local cloned repository (or share a folder tree) to create an exact non-destructive move map. No guessed filenames or remote changes are included in this plan.
