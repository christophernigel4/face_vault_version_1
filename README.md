# Face Vault

Face Vault is a static, browser-only app. It has no server-side build step or database.

## Deploy to Vercel

1. Put `index.html` and `vercel.json` in the root of a Git repository.
2. Push the repository to GitHub, GitLab, or Bitbucket.
3. In Vercel, choose **Add New → Project** and import that repository.
4. Choose **Other** as the framework preset. Leave the build and install commands unset; serve the project root as the output.
5. Deploy, then open the HTTPS URL and allow camera access when prompted.

The page and configuration are the only files required for deployment. Face-api.js and its model files are still loaded from external CDNs, so the first visit and face recognition require an internet connection.

## Data and privacy

Names and face embeddings are stored in IndexedDB in each visitor's own browser. The app does not upload those records to Vercel. Camera access is restricted to this site by the `Permissions-Policy` header.
