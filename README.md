# DANIX Improvements & Access Requests

This repository is used by DANIX Terminal users to submit access requests and improvement suggestions.

## Access requests

The Cloudflare Worker creates an Issue here when a user requests access from DANIX Terminal.

The repository owner reviews the Issue. To approve a user:
1. Copy the exact User ID from the Issue.
2. Add that ID on its own line to `approved-users.txt` in the main `FREE-FIRE-PANEL` repository.
3. Commit the change.

Closing an Issue without adding the ID means the request was not approved.

## Improvement suggestions

Users can open an Issue describing:
- What they want changed or added
- Why the change would be useful
- Any relevant non-sensitive details

## Repository setup

- Keep GitHub Issues enabled (Settings -> General -> Features -> Issues).
- The repository must be accessible to the Cloudflare Worker token.
- The Worker token should have **Issues: Read and write** permission for this repository only.
- Never put GitHub tokens, passwords, or private user data in this repository.

This repository does not contain the Cloudflare Worker secret or the main terminal application.
