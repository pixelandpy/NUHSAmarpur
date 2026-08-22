# NUHSAmarpur — Content Repository

This repository holds the **content** for the N.U.H.S. Amarpur school
website — notices, events, faculty, gallery photos, achievements,
downloads, and the school's own information — as plain JSON files, plus
the photos and PDFs they refer to.

**This repository is not the website itself.** The website's code
(HTML/CSS/JavaScript) is deployed separately on Netlify, at
**`https://nuhsamarpur.netlify.app`**. That website fetches every file
in this repository directly, at runtime, over a plain public HTTPS
request — there is no build step, no deployment, and no connection
between this repository and Netlify. Editing a file here never triggers
anything on Netlify; the website simply reads the current version of the
file the next time someone opens a page.

## Structure

Everything sits flat in this repository's root — **no subfolders** —
so it's easy to add and edit from a phone:

```
school.json          General school info, principal, contact details
notices.json          Notices/announcements
events.json            Events
faculty.json            Teachers/staff
gallery.json             Photo gallery entries
achievements.json         Achievements
downloads.json             Downloadable PDFs/forms

hero.jpg                    Homepage hero photo (this exact filename)
<any other name>.jpg          Any other photo, referenced by filename
                                from the JSON files above
<any other name>.pdf            Any PDF, referenced by filename from
                                  downloads.json or a notice's "attachment"
```

## How to edit

See the main website project's **`CONTENT-GUIDE.md`** and
**`PHONE-EDITING-GUIDE.md`** for the exact JSON format of every file and
step-by-step phone instructions. In short:

1. Open the file you want to change directly in GitHub (web or app) —
   everything is at the top level, no folders to open first.
2. Edit it, then commit.
3. For a new photo or PDF: **Add file → Upload files**, upload it
   straight into this repository's root (no subfolder), commit, then add
   its exact filename to the relevant JSON file.

Changes are usually visible on the live website within a minute or two.

## Keep this repository public

The website reads these files directly from a visitor's browser with no
login and no access token, so this repository needs to stay **public**
for the site to work.
