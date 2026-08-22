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
