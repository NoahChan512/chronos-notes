USE THIS FOLDER / ZIP ONLY

CURRENT FIX: CMS now uses GitHub backend, not Netlify Identity / Git Gateway.

Upload these files/folders to GitHub repo root:
- index.html
- netlify.toml
- admin/
- content/
- assets/

Do NOT upload old zip files. Do NOT upload .git folders.

GitHub repo expected:
NoahChan0512/chronos-notes

After uploading to GitHub:
1. Netlify should redeploy automatically if linked to GitHub.
2. Open https://chronosnotesofficial.netlify.app/admin/
3. Login should use GitHub OAuth, not Netlify invite/password.
4. If Netlify asks for OAuth setup: Netlify User settings → Applications → OAuth applications → callback URL https://api.netlify.com/auth/done.
