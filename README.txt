Nodeway onboarding demo apps
============================
Plain HTML files. No build step, no server code, no external libraries.

Files
  index.html            Launcher page with a link to every app
  gmail_hr.html         Gmail, HR Onboarding mailbox
  gmail_angella.html    Gmail, Angella Smith (HRBP)
  gmail_jessica.html    Gmail, Jessica Reyes (new joinee)
  workday_hrops.html    Workday, HR Operations
  workday_angella.html  Workday, Angella Smith (HRBP), includes the audit trail
  workday_jessica.html  Workday, Jessica Reyes (new joinee)
  adp.html              ADP Workforce Now
  servicenow.html       ServiceNow
  teams.html            Teams
  seek_demo.html        Self-running Seek demo (all apps in one page)
  docs/                 Real PDF attachments (offer letter, ID proof, education
                        certificates) and page images used by the Gmail preview

Host it
  1. Upload the whole folder to any static host, for example GitHub Pages,
     Netlify, Vercel, S3 or your company web server.
  2. Open index.html. Keep all files in the same folder, because the apps
     link to each other with relative paths.

Try it locally
  Open index.html in a browser, or run:  python3 -m http.server 8000
  then visit http://localhost:8000

Notes
  - Every app starts with its tasks pending. Each has a "Reset demo" link.
  - Gmail Jessica has a Refresh button that delivers the welcome email.
    Workday Angella and Workday Jessica have Refresh on their Home page.
  - There is no HRBP approval step. Hire Employee in Workday completes as
    soon as it is submitted. Angella only receives the audit trail.
  - All apps are light mode only, whatever the computer's appearance setting.
  - Attachments open in a Gmail-style preview. Download and "Open in new
    window" use the real PDF files in docs/.
  - Workday opens on Home. Seek can reach Hire Employee from the Hire app,
    the Menu, the Inbox or the search bar (workday_hrops.html#hire opens the
    Hire app directly).
  - ADP starts empty. Process › Hire employee (or adp.html#hire) is a 3-step
    hire: Personal details, Job and pay, Tax and review.
  - ServiceNow opens on the Employee Center Home. Catalog › New Hire IT Bundle
    (or servicenow.html#item) is a 3-step order: Who it's for, Choose items,
    Review and submit.
  - Workday uses search-and-select fields like the real product: type, then
    pick from the list or press Enter. Learning has the buddy picker.
  - All people, IDs and data are fictional. The ID proof is marked SPECIMEN.
