# Chronos Notes CMS — GitHub Backend Setup

This version avoids Netlify Identity / Git Gateway. It uses GitHub login through Netlify OAuth instead.

## Why
If Netlify Identity invite/login buttons do not respond, GitHub backend is cleaner and free.

## Files to upload
Upload this whole folder to GitHub repo:
`NoahChan0512/chronos-notes`

## Netlify settings
1. Netlify → Site configuration → Build & deploy → Continuous deployment → Link to GitHub repo `NoahChan0512/chronos-notes`.
2. Build command: leave blank.
3. Publish directory: `.`
4. Redeploy.

## Netlify OAuth for Decap CMS
1. Netlify → User settings → Applications → OAuth applications.
2. Create new OAuth application.
3. Application name: Chronos Notes CMS
4. Authorization callback URL: `https://api.netlify.com/auth/done`
5. Copy Client ID and Client Secret.
6. Netlify → your site → Site configuration → Environment variables.
7. Add:
   - `OAUTH_CLIENT_ID` = Client ID
   - `OAUTH_CLIENT_SECRET` = Client Secret
8. Redeploy.

## Login
Open:
`https://chronosnotesofficial.netlify.app/admin/`

Click login. It should now use GitHub, not Netlify Identity password.
