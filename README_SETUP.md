# Chronos Notes — Best Free No-Reupload Setup

## Final recommendation
Use **GitHub + Netlify Auto Deploy + Decap CMS**.

Why this is the best free path:
- You edit at `/admin` in a proper CMS interface.
- Saving changes commits to GitHub.
- Netlify auto-deploys the new version.
- No more downloading `index.html` and re-uploading zip files.
- Waiting list still goes to Netlify Forms.

## What you still need to do once
Because this needs your accounts, there is one setup step that Noah must do manually.

### 1. Create GitHub repo
Create a new GitHub repo:

```text
chronos-notes
```

Upload this whole folder to the repo.

### 2. Fix CMS repo setting
Open:

```text
admin/config.yml
```

Change:

```text
repo: YOUR_GITHUB_USERNAME/chronos-notes
```

to your real GitHub repo, e.g.

```text
repo: nokchan/chronos-notes
```

### 3. Connect Netlify to GitHub
In Netlify:

```text
Add new site → Import from GitHub → choose chronos-notes → Deploy
```

Build settings:

```text
Build command: leave blank
Publish directory: .
```

### 4. CMS login
After deploy, open:

```text
https://your-site.netlify.app/admin
```

Login with GitHub.

If GitHub login needs OAuth setup, follow Netlify / Decap prompt. This is a one-time setup.

## After setup, daily use
1. Go to `/admin`
2. Edit:
   - website copy
   - logo
   - IG / Threads links
   - letter password numbers
   - area
   - location clue
   - drop window
3. Click Save / Publish
4. Netlify redeploys automatically

## Waiting list submissions
They go to:

```text
Netlify Dashboard → your site → Forms → chronos-waitlist
```

Turn on email notifications in Netlify Forms if you want instant alerts.

## Important note
This CMS version is better than the one-file version for long-term use, but it needs GitHub + Netlify connected once. If you want zero setup, the old one-file version is easier, but you must re-upload after edits.
