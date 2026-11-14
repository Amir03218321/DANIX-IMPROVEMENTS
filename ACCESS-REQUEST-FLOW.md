# DANIX access request flow

1. DANIX Terminal creates or reads a locally generated User ID.
2. After the user agrees to request access, the terminal sends the User ID and app version to the Cloudflare Worker.
3. The Worker uses its private `GITHUB_TOKEN` secret to create an Issue in this repository.
4. The repository owner reviews the Issue.
5. To approve, the owner adds the exact User ID to `approved-users.txt` in the main `Amir03218321/FREE-FIRE-PANEL` repository.
6. The terminal checks the main repository's approval list. An Issue by itself does not grant access.

## Important

- Do not upload GitHub tokens or secrets.
- Do not approve a user based only on an Issue title; verify the User ID.
- The Worker must be deployed and tested before this flow can work end-to-end.
- Add Cloudflare rate limiting before making the Worker public.
