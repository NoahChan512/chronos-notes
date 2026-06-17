# Chronos Notes CMS login fix

This package fixes the current Decap CMS popup "Not Found" problem.

What changed:
- admin/config.yml now uses `backend: git-gateway` instead of broken GitHub OAuth endpoint.
- admin/index.html now loads Netlify Identity widget.
- index.html also loads Identity widget so invite/reset links do not fall back to a dead homepage.

Upload/commit these files to GitHub, replacing existing files:
- admin/config.yml
- admin/index.html
- index.html

Then Netlify:
1. Site configuration → Identity → Enable Identity
2. Registration: Invite only
3. Services → Git Gateway → Enable Git Gateway
4. Identity → Invite users → invite your email
5. Open invitation email in the same browser, set password
6. Go to https://chronosnotesofficial.netlify.app/admin/
7. Login with email/password, NOT GitHub popup.

Do NOT enable External providers unless you want Google/GitHub login. Email/password is free and enough.
