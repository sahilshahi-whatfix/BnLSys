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
  - Open the apps in the same browser. They pass events to each other:
    email sent from one Gmail mailbox arrives in the other mailbox, and
    finishing the hire and onboarding in Workday HR Operations updates
    Workday Jessica and Workday Angella without any refresh button.
  - To reset everything, double-click the bottom-left corner of any app or
    press Ctrl+Shift+Alt+R. All open tabs reset together.
  - Dates and times follow the computer's clock. The offer letter, start
    date (Jan 1, 2027) and documents are fixed.
  - In the self-running demo, press Shift+F to toggle 2x speed.
  - Gmail Jessica's Refresh icon brings in a prepared welcome email if HR
    hasn't sent one.
  - Workday: Hire Employee completes as soon as it is submitted (no
    approval). The hire form defaults from requisition JR-2026-0417,
    including the location mismatch (On-site vs the offer's Hybrid).
  - ADP: Process > Hire employee is a 3-step hire. ServiceNow: Catalog >
    New Hire IT Bundle is a 3-step order. Items complete on their own.
  - All people, IDs and documents are fictional.
