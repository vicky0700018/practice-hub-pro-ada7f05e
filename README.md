# Practice Hub Pro

https://github.com/vicky0700018/practice-hub-pro

copy this repo

initial prompt
Build a complete high-fidelity SaaS demo/prototype for an Indian CA practice-management application inspired by the provided CAConnect/Bevritti screenshots.

IMPORTANT TECHNOLOGY RESTRICTIONS — MUST FOLLOW EXACTLY:

1. Use React with Vite.
2. Use Tailwind CSS for all styling.
3. Use ONLY React + Vite + Tailwind CSS.
4. DO NOT use any database.
5. DO NOT use Supabase.
6. DO NOT use Firebase.
7. DO NOT create any backend.
8. DO NOT create any API.
9. DO NOT use external APIs.
10. DO NOT use any additional UI/component library.
11. DO NOT use Material UI.
12. DO NOT use shadcn/ui.
13. DO NOT use Chakra UI.
14. DO NOT use Ant Design.
15. DO NOT use Bootstrap.
16. DO NOT use Redux or any state-management library.
17. DO NOT use React Router or any other routing library.
18. If routing is required, implement simple navigation/state-based page switching using React only.
19. DO NOT use icon libraries such as Lucide, Font Awesome, Heroicons, etc.
20. Use simple text symbols, Unicode icons, CSS shapes, or inline SVG only when absolutely necessary.
21. All data must be local mock data inside React files.
22. All CRUD-like interactions should work in frontend state only.
23. Refreshing the page may reset the demo data. That is acceptable.
24. This is a frontend-only functional demo, not a production application.

==================================================
CORE REQUIREMENT
==================================================

Create a polished, realistic, fully clickable CA practice-management dashboard.

The visual design must closely follow the supplied CAConnect screenshots:

- Dark theme
- Near-black/navy background
- Left fixed sidebar
- Thin borders
- Dark cards
- White/off-white typography
- Muted gray secondary text
- Red for overdue/danger
- Green for completed/paid
- Blue for in-progress/invoiced
- Orange/brown alert banners
- Serif-style large page headings
- Compact professional SaaS interface
- Spacious desktop layout
- Responsive on tablet/mobile
- Minimal, professional accounting/CA software appearance

DO NOT redesign the application into a generic modern dashboard.
DO NOT introduce gradients, excessive rounded cards, colorful marketing UI, oversized illustrations, or unnecessary animations.

The screenshots are the visual source of truth.

==================================================
GLOBAL LAYOUT
==================================================

Create a persistent application shell.

LEFT SIDEBAR:

Logo:
CAConnect

Navigation exactly in this order:

1. Dashboard
2. Clients
3. Deadlines
4. Documents
5. Fees
6. TDS Returns
7. Audits
8. Income Tax
9. Advance Tax
10. Notice Tracker
11. GST Reconciliation
12. Client Emails
13. Team
14. Marketplace

Each navigation item must be clickable and open its corresponding page.

Active navigation item:
- darker highlighted rectangular background
- brighter text
- subtle border if required

Top-right header:
- small theme/sun icon using text/inline SVG
- circular avatar with "ST"
- "Sthambhalliance"

Keep the same general header/sidebar proportions as the screenshots.

==================================================
MOCK DATA
==================================================

Use realistic Indian CA/accounting mock data.

Example clients:

- Anand Provision Stores
- Deccan Logistics Pvt Ltd
- Ganesh Steel Works
- Kavita Desai
- Konark Foods
- Meera Kulkarni
- Nikhil Joshi
- Orbit Software Solutions
- Patil Agro Industries
- Sunrise Textiles Pvt Ltd
- Wellness Pharma LLP
- Vaidya Healthcare LLP
- Tushar Kumar
- Sneha Kulkarni
- Santosh Kumar

Use realistic but clearly fictional:
- PAN
- GSTIN
- email
- phone
- dates
- amounts
- financial years

Do not use real person's sensitive information.

==================================================
1. DASHBOARD
==================================================

Page title:

Good morning, Sthambhalliance

Subtitle:

What needs your attention today.

Top quick action buttons:

+ Add client
+ Request docs
+ Log fee
Draft a notice reply

These buttons must actually open the corresponding modal/page.

Alert 1:

1 new demand raised this week · ₹13,17,699.50 outstanding across 10 clients

Alert 2:

1 client short on advance tax · ₹5,52,500 in interest exposure so far

KPI CARDS:

1. Overdue filings
   24

2. Due in 7 days
   14

3. Clients
   22

4. Fees overdue
   ₹12,000

Needs attention section:

Heading:
Needs attention

Right:
View all deadlines

Subheading:
Overdue · 24 · Past the due date — deal with these first

Create filing rows.

Each row must contain:

- Filing/service name
- Period/FY
- Client
- Days overdue
- Due date
- Status badge
- Start button
- More (...) action

Example:

GSTR-1 — May 2026
Tushar Kumar
96 days overdue
11 Jun 2026
Overdue
Start
...

GSTR-3B — May 2026
Tushar Kumar
87 days overdue
20 Jun 2026
Overdue
Start
...

GSTR-1 — Jun 2026
Tushar Kumar
66 days overdue
11 Jul 2026
Overdue
Start
...

GSTR-3B — Jun 2026
Tushar Kumar
57 days overdue

ITR filing (non-audit)
Tushar Kumar
46 days overdue
31 Jul 2026
Overdue
Start

TDS return (26Q)
Ganesh Steel Works
46 days overdue
31 Jul 2026
In Progress
Mark filed

Clicking Start / Mark filed must update mock state.

==================================================
2. CLIENTS
==================================================

Page:

Clients

22 clients

Top-right:
+ Add client

Search input placeholder EXACTLY:

Search by name, PAN or GSTIN

Filter:
All services

Client table columns:

Name
Type
PAN
Services
...

Example rows:

Anand Provision Stores
Partnership Firm
AAIFA5678V
GSTR-1, GSTR-3B

Deccan Logistics Pvt Ltd
Company
AAKC03456Y
GSTR-1, GSTR-3B, ROC

Ganesh Steel Works
Partnership Firm
AAGFG8901T
GSTR-1, GSTR-3B, TDS

Kavita Desai
Individual
ABCPD1234M
ITR

Meera Kulkarni
Individual
BNZPK3456S
ITR

Nikhil Joshi
Individual
AKJPJ9012P
ITR, TDS

Orbit Software Solutions
Company
AAHC02345U
GSTR-1, GSTR-3B, ROC, TDS, ITR

Each row has (...) action.

Search and service filter must work.

==================================================
ADD CLIENT MODAL — EXACT FIELDS
==================================================

When + Add client is clicked, open a scrollable modal.

Modal title:

Add client

Description:

Only the name is required — you can fill in the rest later.

Fields EXACTLY:

Client name *
Text input

Client type
Dropdown

KYC entity type *
Dropdown

Helper text:

Creates the right KYC checklist after the client is added

PAN
Text input
Placeholder:
ABCDE1234F

Helper:
Optional. e.g. ABCDE1234F

GSTIN
Text input
Placeholder:
27ABCDE1234F1Z5

Helper:
Optional. 15 characters, e.g. 27ABCDE1234F1Z5

Email
Text input
Placeholder:
client@example.com

Phone
Text input
Placeholder:
98765 43210

Helper:
Used for the WhatsApp document link

Services

Checkbox cards:

ITR
GSTR-1
GSTR-3B
TDS
ROC
Company Registration
Advance Tax
Other

Notes
Textarea

Placeholder:
Anything worth remembering

Buttons:

Cancel
Add client

Client name and KYC entity type must be required.

On Add client:
- validate required fields
- add client to local React state
- show success feedback using a simple inline/toast-like message made without a library
- close modal
- update client count/table

==================================================
3. DEADLINES
==================================================

Page title:

Deadlines

Subtitle/count:

24 overdue · 88 open

Top-right:

+ Add deadline

Filters:

All clients
All services
Show filed checkbox

Section:

Overdue · 24 · Past the due date — deal with these first

Rows contain:

- Service
- Period/FY
- Client
- Days overdue
- Due date
- Status
- Start / Mark filed
- ...

Use examples:

GSTR-1 — May 2026
Tushar Kumar
96 days overdue
11 Jun 2026
Overdue

GSTR-3B — May 2026
Tushar Kumar
87 days overdue
20 Jun 2026
Overdue

GSTR-1 — Jun 2026
Tushar Kumar
66 days overdue
11 Jul 2026
Overdue

GSTR-3B — Jun 2026
Tushar Kumar
57 days overdue
20 Jul 2026
Overdue

ITR filing (non-audit)
ITR
AY 2026-27
Tushar Kumar
46 days overdue
31 Jul 2026

TDS return (26Q)
TDS
Q1 FY2026-27
Ganesh Steel Works
46 days overdue
31 Jul 2026
In Progress
Mark filed

==================================================
ADD ONE-OFF DEADLINE MODAL
==================================================

Title:

Add a one-off deadline

Description:

For dates the compliance calendar cannot know — a notice reply-by date, a hearing, and ad-hoc filing.

Fields:

Client *
Dropdown
Placeholder:
Choose a client

What is due *
Text input
Placeholder:
Reply to 143(2) notice

Service
Dropdown
Default:
Other

Due date *
Date input
Placeholder:
dd-mm-yyyy

Notes
Textarea

Buttons:

Cancel
Add deadline

Adding a deadline must add it to local state.

==================================================
4. DOCUMENTS
==================================================

Page title:

Documents

Subtitle:

4 links awaiting upload

Top-right:

+ Request documents

Tabs:

Requests (6)
Files (1)

Requests table columns:

Request
Client
Received
Expires
Status

Actions:
Share
Cancel/Delete

Example data:

Company Registration
Tushar Kumar
1 of 4
19 Sept 2026
Completed

KYC documents
Tushar Kumar
0 of 5
21 Sept 2026
Open

ITR — Salaried
Deccan Logistics Pvt Ltd
0 of 2
13 Oct 2026
Open

GST — Monthly
Kavita Desai
0 of 3
05 Oct 2026
Open

GST — Monthly
Nikhil Joshi
0 of 3
12 Sept 2026
Expired

GST documents — Aug 2026
Sunrise Textiles Pvt Ltd
0 of 2
30 Sept 2026
Open

Statuses:
Completed
Open
Expired

==================================================
REQUEST DOCUMENTS MODAL
==================================================

Title:

Request documents

Description:

Your client gets a link they can upload from — no login required.

Fields:

Client *

Dropdown:
Choose a client

Start from a checklist

Buttons/options:

ITR — Salaried
GST — Monthly
Company Registration

Title *

Placeholder:
ITR 2026-27 documents

Documents needed *

Initial item:
Form 16

Required checkbox

Delete item

+ Add item

Message (optional)

Textarea

Placeholder:
Please send these by Friday so we can file on time.

Link expires in (days)

Default:
30

Helper:
Links are time-limited so an old one cannot be reused

Buttons:

Cancel
Create link

Create link should add a request to local state.

==================================================
5. FEES
==================================================

Page title:

Fees

Subtitle:

What you have billed and what has come in.

Top-right:

+ Log fee

KPI cards:

Collected this month
₹19,000

Outstanding
₹22,790

Overdue · 1
₹12,000

Tabs/filters:

All
Invoiced
Overdue
Paid
Draft

Table columns:

For
Client
Amount
Due
Status
...

Example rows:

ITR filing
ITR
Nikhil Joshi
₹1,290
Invoiced

GST monthly retainer — Aug 2026
GSTR-3B
Sunrise Textiles Pvt Ltd
₹7,500
Paid

ITR filing AY 2026-27
ITR
Kavita Desai
₹3,500
Paid

ROC annual filing FY 2025-26
ROC
Orbit Software Solutions
₹12,000
10 Sept 2026
Overdue

ITR filing AY 2026-27
ITR
Meera Kulkarni
₹3,500
Paid

TDS quarterly filing Q1
TDS
Vaidya Healthcare LLP
₹4,500
18 Sept 2026
Invoiced

GST monthly retainer — Aug 2026
GSTR-3B
Ganesh Steel Works
₹5,500
Paid

==================================================
LOG A FEE MODAL
==================================================

Title:

Log a fee

Description:

Track what you have billed and what has come in.

Fields:

Client *
Dropdown
Choose a client

For what *
Text input

Amount (₹) *
Text/number input
Placeholder:
2500

Helper:
e.g. 2500 or 2,500.50

Service
Dropdown
Default:
No service

Status
Dropdown
Options:
Invoiced
Paid
Overdue
Draft

Due date
Date input
Placeholder:
dd-mm-yyyy

Helper:
Overdue is worked out from this

Buttons:

Cancel
Log fee

==================================================
6. TDS RETURNS
==================================================

Page title:

TDS Returns

Subtitle:

Challans and deductees for every 24Q and 26Q, with the common filing mistakes flagged before you file.

Left card:

Open a return

Fields:

Client *
Dropdown

Financial year *
Dropdown

Quarter *
Dropdown

Form *
Dropdown

Default example:
24Q — Salary

Helper:

24Q — salary. 26Q — everything else.

Button:

Open return

Right:

All returns

Table:

Client
Quarter
Form
TDS total
Flags
Status

Example:

Ganesh Steel Works
Q2 FY2026-27
26Q
₹750
1
Preparation

Deccan Logistics Pvt Ltd
Q2 FY2026-27
26Q
₹0
0
Filed

==================================================
7. AUDITS
==================================================

Page title:

Audits

Subtitle:

Workpapers, evidence and sign-off for every tax, statutory and GST audit the firm is running.

Left card:

Open an engagement

Fields:

Client *
Dropdown
Select a client

Audit type *
Dropdown
Choose an audit

Helper:

Loads that audit's checklist into the file.

Financial year *
Dropdown

Default:
FY2026-27

Button:

Open engagement

Right:

All engagements

Table columns:

Client
Audit
Year
Progress
Assigned
Due
Status

Examples:

Wellness Pharma LLP
GST
FY2025-26
6/15 done
Planning

Kavita Desai
Statutory
FY2025-26
0/24 done
Planning

Ganesh Steel Works
Statutory
FY2025-26
1/24 done
Planning

Progress bars should be made using Tailwind CSS only.

==================================================
8. INCOME TAX
==================================================

Page title:

Income Tax status

Subtitle:

Refunds, demands and return processing across every client, with anything that changed since your last check flagged.

Information banner:

Automated sync is not connected. The Income Tax Department has no public API — the lawful automated route is ERI registration, which a firm applies for separately. Until then, record what you see on the portal or import a demand register you have downloaded; everything below works the same either way.

KPI section:

Outstanding demand
₹13,17,699.50

Clients with demands
10

Refunds awaited
₹0

New demands this week
1

Left card:

Import a demand register

Field:

Demand register *

Browse file input

Helper:

Columns: pan, assessment_year, amount, and optionally din, section, raised_on.

Button:

Import register

Helper text explaining that imported register replaces outstanding demands for each PAN.

Right section tabs:

Alerts (1)
Refunds
Demands

Alert examples:

Sumit Kumar
AY2025-26
New demand of ₹18,600 under 143(1).
08 Sept

Sanjay Bhosale
AY2024-25
New demand of ₹74,500.50 under 154.
07 Sept

Rajesh Kulkarni & Sons
AY2024-25
New demand of ₹9,999 under 234C.
07 Sept

Priya Sharma
AY2025-26
New demand of ₹1,05,000 under 143(1).
07 Sept

Meera Kulkarni
AY2024-25

Button:

Mark 1 as seen

Implement local file-selection simulation. No real backend upload is needed.

==================================================
9. ADVANCE TAX
==================================================

Page title:

Advance Tax

Subtitle:

An estimate per client per year, checked against the four statutory dates — 15% by 15 Jun, 45% by 15 Sep, 75% by 15 Dec, 100% by 15 Mar.

KPI:

Clients short right now
1

Total interest exposure
₹5,52,500

Due within 7 days
0

Next installment, firm-wide
—

Left card:

Open an estimate

Fields:

Client *
Dropdown
Select a client

Financial year *
Dropdown
FY2026-27

Estimated tax liability for the year (₹) *
Number input
Placeholder:
e.g. 5,00,000

Helper:

After TDS/TCS already credited elsewhere — the net figure advance tax is actually computed on. Applies once this exceeds ₹10,000 (s.208).

Button:

Save estimate

Right:

All estimates

Table:

Client
FY
Estimated
Paid
Next due
Status

Example:

Anand Provision Stores
FY2025-26
₹50,00,000
₹4,00,000
All due
Short

==================================================
10. NOTICE TRACKER
==================================================

Page title:

Notice Tracker

Subtitle:

₹10,000 in open matters.

Top-right:

Draft a reply
+ Add matter

Table:

Notice
Client
Drafted
Status
Delete

Example:

FY-2025-26 Scrutiny notice
GST audit
Deccan Logistics Pvt Ltd
06 Sept 2026, 01:10 am
Received

143(2) scrutiny — Sunrise Textiles
—
05 Sept 2026, 07:46 pm
Draft

Statuses:
Received
Draft

Delete action must work on local state.

==================================================
11. ADD NOTICE MATTER
==================================================

Page title:

Add notice matter

Subtitle:

Track deadlines, hearings and the complete notice lifecycle.

Card:

Matter details

Fields:

Client *
Dropdown
Choose a client

Matter title *
Text input
Placeholder:
FY 2025-26 scrutiny notice

Notice type *
Dropdown
Choose type

Notice date *
Date input
dd-mm-yyyy

Response deadline
Date input
dd-mm-yyyy

Amount in dispute (₹)
Number input
Default:
0.00

Initial note
Textarea
Placeholder:
What needs attention?

Button:

Add matter

Adding must update Notice Tracker local state.

==================================================
12. GST RECONCILIATION
==================================================

Page title:

GST Reconciliation

Subtitle:

Compare purchase registers against GSTR-2B and resolve mismatches before filing.

Left card:

New reconciliation

Fields:

Client *
Dropdown
Select a client

Month *
Month input
Placeholder:
--------, ----

Helper:

The GST return period, e.g. 2025-06

Purchase register *
File input

Helper:

CSV with columns: supplier_gstin, invoice_number, invoice_date, invoice_amount

GSTR-2B JSON *
File input

Helper:

Download from the GST portal → Returns → GSTR-2B → Download JSON

Button:

Run reconciliation

Right:

Past runs

Initial empty state:

Icon/symbol
No reconciliations yet

Upload a purchase register and GSTR-2B to run your first comparison.

When mock files are selected and Run reconciliation is clicked, show a simulated reconciliation result using local state.

Create a professional result view containing:
- matched invoices
- mismatched invoices
- missing invoices
- totals
- ITC difference

No backend or real GST API.

==================================================
13. CLIENT EMAILS
==================================================

Page title:

Client Emails

Subtitle:

AI-drafted updates and reminders for your clients.

Top-right:

Draft an email

Initial empty state:

No client emails yet

Pick a client and a topic, and let AI draft the note for you.

Button:

Draft an email

==================================================
DRAFT CLIENT EMAIL PAGE
==================================================

Title:

Draft a client email

Subtitle:

Pick a client and a topic — the facts come from your own records.

Fields:

Client *
Dropdown
Choose a client

Topic *
Dropdown
Initially disabled until client selected

Additional notes (optional)
Textarea

Placeholder:
Mention that the due date was recently extended...

Button:

Draft email

Right side:

Draft

Empty state:

Your draft will appear here

Pick a client and a topic, then hit Draft email.

Since there is no API/AI backend, simulate AI drafting using predefined local templates based on selected topic.

After clicking Draft email, display a realistic editable email draft.

==================================================
14. TEAM
==================================================

Page title:

Team

Subtitle:

Who can work in Sthambhalliance.

Section:

People (1)

Top-right:

Invite someone

Table columns:

Person
Role
Joined

Example:

Santosh Kumar
Owner
05 Sept 2026

Section:

Pending invitations (3)

Table:

Email
Expires

Each row:
- copy invitation action
- cancel action

Example mock emails can be fictional.

Invite someone should open a modal.

Invite modal fields:

Email *
Role

Buttons:
Cancel
Send invitation

Adding invitation updates pending invitations locally.

==================================================
15. MARKETPLACE
==================================================

Page title:

Marketplace

Subtitle:

Your firm is listed publicly. Clients can find you and request work.

Tabs:

Listing
Packages (3)
Bookings (1 new)
Reviews (1)

Make each tab clickable.

BOOKINGS tab should reproduce the screenshot structure.

Booking card:

Client name
Status badge

Client email
Phone
City

Requested service
Request date

Right side:
Service amount
Platform fee
Platform fee information

Example requested booking:

Santosh Kumar
requested

santosh@gmail.com
8653453432
New Delhi

ITR filing — salaried or freelancer
13 Sept 2026

₹2,500

₹200 platform fee
from the client, not you · not charged yet

Buttons:

Accept
Decline

When accepted:

Santosh Kumar
accepted
In your clients

₹15,000

₹1,200 platform fee
from the client, not you · not charged yet

Button:

Mark complete

Helper:

Marking it complete is what lets the client leave a review.

Another accepted example:

Sneha Kulkarni
accepted
In your clients

sneha.kulkarni@example.com
9820044556
Pune

GST monthly compliance
05 Sept 2026

Message:

We are a 12-person design studio, just crossed the GST threshold. Need monthly filing handled from October.

₹5,000

₹400 platform fee
from the client, not you · not charged yet

Button:
Mark complete

Accept / Decline / Mark complete must update local React state.

LISTING TAB:
Create a professional firm listing view using the same visual language.
Keep it simple and realistic.

PACKAGES TAB:
Show 3 mock service packages.

REVIEWS TAB:
Show 1 mock client review.

==================================================
GLOBAL INTERACTIONS
==================================================

This must be a FUNCTIONAL FRONTEND DEMO, not static screenshots.

Implement:

- Sidebar navigation
- Search
- Filters
- Tabs
- Dropdowns
- Checkboxes
- Date inputs
- File inputs with local simulated selection
- Add client
- Add deadline
- Request documents
- Log fee
- Open TDS return
- Open audit engagement
- Import demand register simulation
- Save advance tax estimate
- Add notice
- Run GST reconciliation simulation
- Draft email simulation
- Invite team member
- Marketplace Accept
- Marketplace Decline
- Marketplace Mark complete
- Delete actions
- More (...) menus
- Status changes
- Modal open/close
- Form validation
- Empty states
- Success/error messages

All interactions must use React state.

==================================================
MODALS
==================================================

Create reusable modal behavior using React components and Tailwind.

Do NOT use any modal/dialog library.

Modal characteristics:
- centered
- dark background
- border
- backdrop overlay
- close X
- scrollable when content is long
- footer buttons
- consistent spacing

==================================================
DESIGN SYSTEM
==================================================

Use Tailwind CSS only.

Background:
very dark navy/black.

Sidebar:
slightly lighter dark navy.

Cards:
dark gray/navy with subtle borders.

Borders:
thin and low contrast.

Typography:
- large elegant serif headings similar to screenshot
- clean sans-serif body text
- muted secondary text

Buttons:
- off-white primary buttons
- dark bordered secondary buttons
- compact height
- subtle hover state

Status colors:
- red = overdue/error
- green = paid/completed
- blue = in progress/invoiced
- gray = draft/open/planning
- orange/brown = warnings

Do not use gradients.

Do not make every element excessively rounded.

Use modest border radius similar to screenshots.

==================================================
RESPONSIVE BEHAVIOR
==================================================

Desktop is the primary design target.

Also make the application responsive.

Desktop:
- fixed sidebar
- main content fills remaining width

Tablet:
- narrower sidebar
- content adapts

Mobile:
- sidebar becomes a compact collapsible navigation
- tables become horizontally scrollable
- cards stack
- modals fit viewport
- forms become single-column

==================================================
FILE STRUCTURE
==================================================

Keep the project simple.

Use a structure similar to:

src/
  App.jsx
  main.jsx
  index.css
  components/
    Layout.jsx
    Sidebar.jsx
    Header.jsx
    Modal.jsx
    Button.jsx
    Badge.jsx
    Table.jsx
    FormField.jsx
  pages/
    Dashboard.jsx
    Clients.jsx
    Deadlines.jsx
    Documents.jsx
    Fees.jsx
    TDSReturns.jsx
    Audits.jsx
    IncomeTax.jsx
    AdvanceTax.jsx
    NoticeTracker.jsx
    GSTReconciliation.jsx
    ClientEmails.jsx
    Team.jsx
    Marketplace.jsx
  data/
    mockData.js

Do not add unnecessary architecture.

==================================================
IMPORTANT NO-CHANGE RULE
==================================================

The provided screenshots are the source of truth.

DO NOT:
- remove any visible field
- rename any visible field
- merge fields
- simplify forms
- remove buttons
- remove tabs
- remove table columns
- remove sidebar modules
- replace modules with generic placeholders
- invent a different navigation structure
- replace the CAConnect visual style with another style

If a field or behavior is explicitly shown in the screenshots, reproduce it.

Where a page detail was not visible in the screenshots, use a minimal professional implementation consistent with the existing application instead of changing the visible parts.

==================================================
DEMO DATA CONSISTENCY
==================================================

Keep mock data connected across modules.

For example:

If a new client is added:
- it should appear in Clients
- it should become available in client dropdowns in Deadlines
- Documents
- Fees
- TDS
- Audits
- Income Tax
- Advance Tax
- Notice Tracker
- GST Reconciliation
- Client Emails
- Marketplace where applicable

If a fee is added:
- Fees table updates
- dashboard fee summary can update

If a deadline is marked filed:
- its status changes
- dashboard overdue count can update

Use derived values where practical, but do not over-engineer.

==================================================
FINAL QUALITY REQUIREMENTS
==================================================

The finished result should feel like a real CA practice-management SaaS demo.

It must NOT feel like:
- a wireframe
- a static HTML page
- a generic admin dashboard
- a collection of disconnected pages

It should feel like one connected application.

Every sidebar item must work.

Every major button must do something.

Forms must open.

Forms must validate.

Data must update in local React state.

Tables must show realistic mock data.

The visual appearance should closely match the provided CAConnect screenshots.

Most importantly:

THIS IS A FRONTEND DEMO ONLY.

Use:
React
Vite
Tailwind CSS

Nothing else.

NO DATABASE.
NO BACKEND.
NO API.
NO SUPABASE.
NO FIREBASE.
NO EXTERNAL LIBRARIES.
NO EXTERNAL UI LIBRARIES.
NO ICON LIBRARIES.

Use mock data and React state only.


What's in place now: the repo's dark CAConnect look and full mock data (22 clients, deadlines, documents, fees, TDS, audits, income tax, advance tax, notices, marketplace, team), plus the reusable building blocks — buttons, badges, tables, form fields, pop-ups, toasts, progress bars — the shared state that connects every screen, the four main pop-up forms (add client, add deadline, request documents, log fee, invite someone), and the sidebar/header shell with all 14 menu items wired up.

Still unfinished and untested: 
the 14 individual screens themselves (Dashboard through Marketplace) are referenced by the shell but not yet written, so the app will not display until they are added. Nothing has been checked in the live preview yet.

clone the repo and work still unfinished and untested  continue

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/30c0966f-57da-4b6e-82e7-6b7521d1fad5).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
