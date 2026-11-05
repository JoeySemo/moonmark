# Maasverse Reading Companion

The public pages for **Maasverse Reading Companion**, a spoiler-free reading
companion for iOS: tell it where you are in a book and it shows you only what
you have already read.

This repository holds the website only — a landing page and the privacy
policy, served by GitHub Pages. The app itself is not open source and lives
elsewhere.

- [Privacy policy](https://joeysemo.github.io/moonmark/privacy.html)

The `moonmark` path is from an earlier name for the app. The URL is already
published in App Store Connect and in the app itself, so it stays as it is;
renaming the repository would break both.

## Keep-alive

`.github/workflows/keep-supabase-awake.yml` queries the app's backend once a
day. Supabase pauses Free-plan projects after about a week without user
activity, and a paused backend makes the app look empty rather than broken —
which nobody reports, they just stop using it. The run fails loudly on
anything but HTTP 200, so it doubles as an uptime check.

It is a workaround. The fix is the Supabase Pro plan, which is never paused
and also keeps daily backups of readers' progress; this job keeps the lights
on but protects no data. Note too that GitHub disables scheduled workflows in
a repository with no commits for 60 days.

Maasverse Reading Companion is unofficial and fan-made. It is not affiliated
with, endorsed by, or connected to any author or publisher.
