# ICRTACM Conference Website — Standardised Update Prompt

**How to use this file:**
1. Open this file in any text editor
2. Fill in every field under "INPUT: CONFERENCE DATA" below
3. Paste the entire contents of `index.html` into an AI assistant (Claude, ChatGPT, etc.)
4. Paste this filled-in prompt after the HTML
5. The AI will return a fully updated `index.html` ready to deploy

---

---

# ═══════════════════════════════════════════════════════════
# SYSTEM INSTRUCTION FOR AI — DO NOT EDIT THIS SECTION
# ═══════════════════════════════════════════════════════════

You are a web developer maintaining the ICRTACM conference website template
for REVA University. The user has pasted the full `index.html` source code
above this prompt, followed by a filled-in data form below.

Your task is to produce a **complete, updated `index.html`** by applying
every data field from the form to the correct location in the HTML.

## Rules you must follow

1. **Return the complete file** — do not summarise, do not truncate, do not
   use placeholders like "rest of code here". Output the entire HTML from
   `<!DOCTYPE html>` to `</html>`.

2. **Change only what is in the form** — do not alter any CSS, JavaScript,
   layout structure, class names, or comments that are not related to the
   data fields provided.

3. **Apply every field** — if a field says "TBD", write `TBD` in the HTML.
   If a field has a value, replace the old value everywhere it appears.

4. **Speaker cards** — rebuild the entire `<div class="spk-grid">` block
   using only the speakers listed in the form. If fewer than 8 are provided,
   only generate cards for those that are given. If a speaker has no photo
   path, use the fallback avatar (do not invent a filename).

5. **Dates** — replace ALL occurrences of old dates across every section:
   hero pills, ticker, Important Dates table, CFA deadlines sidebar,
   countdown timer target, footer copyright, and page `<title>`.

6. **Links** — replace ALL occurrences of old Google Form URLs and WhatsApp
   links throughout the entire file (navbar register button, hero CTA,
   registration page, contact page).

7. **Edition increment** — update "7th Edition", "7th International", and
   "ICRTACM-2026" everywhere they appear to match the new edition number
   and year provided in the form.

8. **Preserve the brand system** — do not change any CSS variable values
   (`--reva-orange`, `--reva-navy`, fonts, etc.) unless the form explicitly
   provides new brand values.

9. **Validate output** — before returning, mentally verify:
   - `<title>` is updated
   - `meta description` is updated
   - countdown `new Date(...)` target is updated
   - all `TBD` fields are filled where data was provided
   - all speaker cards match the provided list
   - no old edition year (2026) remains unless the new year is also 2026

---

---

# ═══════════════════════════════════════════════════════════
# INPUT: CONFERENCE DATA — FILL EVERYTHING BELOW THIS LINE
# ═══════════════════════════════════════════════════════════
# Instructions:
#   - Replace the placeholder values (inside [ square brackets ])
#   - If a value is not yet decided, write: TBD
#   - If a field should be removed entirely, write: REMOVE
#   - Do not delete any field label — the AI needs the labels to know
#     where to apply each value
# ═══════════════════════════════════════════════════════════


## ── SECTION 1: CONFERENCE IDENTITY ──────────────────────────────────────

CONFERENCE_ACRONYM:        [e.g. ICRTACM-2027]
EDITION_NUMBER:            [e.g. 8th]
EDITION_ORDINAL_WORD:      [e.g. Eighth]
CONFERENCE_YEAR:           [e.g. 2027]
CONFERENCE_FULL_NAME:      [e.g. International Conference on Recent Trends in Applied and Computational Mathematics]
ORGANISING_DEPARTMENT:     [e.g. Department of Mathematics, School of Applied Sciences]
ORGANISING_INSTITUTION:    [e.g. REVA University]
INSTITUTION_CITY:          [e.g. Bangalore, Karnataka, India]


## ── SECTION 2: DATES ─────────────────────────────────────────────────────
# Use format: DDth Month, YYYY  (e.g. 20th May, 2027)
# For date ranges use: DD-DD Month, YYYY  (e.g. 28-29 October, 2027)

CONFERENCE_DATE_DISPLAY:      [e.g. October 28-29, 2027]
CONFERENCE_DATE_DAY1_DISPLAY: [e.g. October 28, 2027]
CONFERENCE_DATE_DAY2_DISPLAY: [e.g. October 29, 2027]

# ISO format for countdown timer — YYYY-MM-DDTHH:MM:SS+05:30
CONFERENCE_DATE_ISO:          [e.g. 2027-10-28T09:00:00+05:30]

REGISTRATION_OPEN_DATE:       [e.g. 20th May, 2027     OR   TBD]
ABSTRACT_SUBMISSION_DATE:     [e.g. 20th September, 2027   OR   TBD]
REGISTRATION_LAST_DATE:       [e.g. 6th October, 2027   OR   TBD]
ABSTRACT_ACCEPTANCE_DATE:     [e.g. 30th September, 2027   OR   TBD]
FULL_PAPER_SUBMISSION_DATE:   [e.g. 6th October, 2027   OR   TBD]


## ── SECTION 3: VENUE ─────────────────────────────────────────────────────

VENUE_NAME:         [e.g. School of Applied Sciences, REVA University]
VENUE_ADDRESS_LINE1:[e.g. Rukmini Knowledge Park, Kattigenahalli]
VENUE_ADDRESS_LINE2:[e.g. Yelahanka, Bangalore, Karnataka - 560 064, India]
CONFERENCE_MODE:    [e.g. Offline (In-Person)   OR   Hybrid   OR   Online]

# Google Maps search query — use + instead of spaces
# Example: REVA+University,+Rukmini+Knowledge+Park,+Kattigenahalli,+Bangalore+560064
MAPS_QUERY:         [e.g. REVA+University,+Rukmini+Knowledge+Park,+Kattigenahalli,+Yelahanka,+Bangalore,+Karnataka+560064]
MAPS_ZOOM_LEVEL:    [e.g. 16]


## ── SECTION 4: REGISTRATION FEES ────────────────────────────────────────
# Write REMOVE against any category to hide that row

FEE_INDUSTRY:           [e.g. Rs. 3,500 /-]
FEE_FACULTY:            [e.g. Rs. 2,000 /-]
FEE_RESEARCH_SCHOLAR:   [e.g. Rs. 1,500 /-]
FEE_PG_UG_STUDENT:      [e.g. Rs. 750 /-]
FEE_INTERNATIONAL_USD:  [e.g. $ 150]

# Note shown below the fees table
FEE_NOTE:  [e.g. International participants use USD. Fee is based on citizenship, not nationality.]


## ── SECTION 5: BANK / PAYMENT DETAILS ───────────────────────────────────

BANK_ACCOUNT_NAME:   [e.g. REVA University]
BANK_NAME_BRANCH:    [e.g. The Karnataka Bank Ltd, REVA University Branch]
BANK_ACCOUNT_NUMBER: [e.g. 6662500101008701]
BANK_IFSC_CODE:      [e.g. KARB0000666]
BANK_SWIFT_CODE:     [e.g. KARBINBBBNG]


## ── SECTION 6: EXTERNAL LINKS ───────────────────────────────────────────

GOOGLE_FORM_URL:      [e.g. https://forms.gle/NEWFORMID123]
WHATSAPP_GROUP_URL:   [e.g. https://chat.whatsapp.com/NEWGROUPLINK   OR   REMOVE]
REVA_PAYMENT_URL:     [e.g. https://www.reva.edu.in/payment]
BROCHURE_PATH:        [e.g. ./assets/docs/brochure.pdf   OR   TBD]


## ── SECTION 7: CONTACT & ORGANISING TEAM ────────────────────────────────
# Repeat ORGANISER blocks as needed (copy the block for each person)
# ROLE options: Convenor | Organising Secretary | Co-Organiser | Treasurer

ORGANISER_1_NAME:       [e.g. Dr. Udaya Kumara K. N.]
ORGANISER_1_ROLE:       [e.g. Convenor]
ORGANISER_1_TITLE:      [e.g. Professor, School of Applied Sciences (Mathematics), REVA University]
ORGANISER_1_PHONE:      [e.g. +91-9980923283]
ORGANISER_1_EMAIL:      [e.g. udayakumarkn@reva.edu.in]

ORGANISER_2_NAME:       [e.g. Dr. Vishu Kumar M.]
ORGANISER_2_ROLE:       [e.g. Organising Secretary]
ORGANISER_2_TITLE:      [e.g. Professor & Head, Department of Mathematics, SAS, REVA University]
ORGANISER_2_PHONE:      [e.g. +91-9845871372]
ORGANISER_2_EMAIL:      [e.g. vishukumarm@reva.edu.in]

ORGANISER_3_NAME:       [e.g. Dr. Hanumagowda B. N.]
ORGANISER_3_ROLE:       [e.g. Organising Secretary]
ORGANISER_3_TITLE:      [e.g. Professor & Head, Department of Mathematics, SAS, REVA University]
ORGANISER_3_PHONE:      [e.g. +91-7760558562]
ORGANISER_3_EMAIL:      [e.g. hanumagowda.bn@reva.edu.in]

# Add more organisers by copying the block above and numbering them 4, 5, 6 ...

GENERAL_CONTACT_EMAIL:  [e.g. icrtacm@reva.edu.in]
GENERAL_CONTACT_PHONE:  [e.g. +91-9980923283]


## ── SECTION 8: COMMITTEE — PATRONS & CHIEFS ─────────────────────────────
# ROLE options: Chief Patron | Patron | Co-Patron

PATRON_1_ROLE:    [e.g. Chief Patron]
PATRON_1_NAME:    [e.g. Dr. P. Shyama Raju]
PATRON_1_TITLE:   [e.g. Hon'ble Chancellor, REVA University]

PATRON_2_ROLE:    [e.g. Chief Patron]
PATRON_2_NAME:    [e.g. Sri. Umesh Raju]
PATRON_2_TITLE:   [e.g. Pro Chancellor, REVA University]

PATRON_3_ROLE:    [e.g. Patron]
PATRON_3_NAME:    [e.g. Dr. Sanjay Chitnis]
PATRON_3_TITLE:   [e.g. Vice-Chancellor, REVA University]

PATRON_4_ROLE:    [e.g. Patron]
PATRON_4_NAME:    [e.g. Dr. K. S. Narayana Swamy]
PATRON_4_TITLE:   [e.g. Registrar, REVA University]

# Add more patrons by copying the block above and numbering them 5, 6 ...


## ── SECTION 9: COMMITTEE — ORGANISING MEMBERS ───────────────────────────
# These appear in the "Organising Committee" tab of the Committees section

COMM_ORG_1_NAME:    [e.g. Prof. Shilpa B. R.]
COMM_ORG_1_ROLE:    [e.g. Deputy Director, School of Applied Sciences, REVA University]
COMM_ORG_1_PHONE:   [e.g. TBD   OR   REMOVE]
COMM_ORG_1_EMAIL:   [e.g. TBD   OR   REMOVE]

COMM_ORG_2_NAME:    [e.g. Dr. Vishu Kumar M.]
COMM_ORG_2_ROLE:    [e.g. Professor & Head, Dept. of Mathematics, SAS, REVA University]
COMM_ORG_2_PHONE:   [e.g. +91-9845871372]
COMM_ORG_2_EMAIL:   [e.g. vishukumarm@reva.edu.in]

# Add more by copying the block above and numbering 3, 4, 5 ...


## ── SECTION 10: COMMITTEE — LOCAL ADVISORY ──────────────────────────────

COMM_LOC_1_NAME:    [e.g. Dr. Madhusudhan Reddy]
COMM_LOC_1_ROLE:    [e.g. Professor & Head, Dept. of Chemistry, REVA University]

COMM_LOC_2_NAME:    [e.g. Dr. Sunitha D. V.]
COMM_LOC_2_ROLE:    [e.g. Professor & Head, Dept. of Physics, REVA University]

COMM_LOC_3_NAME:    [e.g. Dr. Sikandar Mulla]
COMM_LOC_3_ROLE:    [e.g. Associate Professor & Head (I/C), Dept. of Biochemistry, REVA University]

# Add more by copying the block above and numbering 4, 5 ...


## ── SECTION 11: COMMITTEE — NATIONAL / INTERNATIONAL ADVISORY ───────────
# List each member as: NAME | ROLE (institution, country)

COMM_INTL_1:  [e.g. Dr. Hari Ponnamma Rani | Professor, Dept. of Mathematics, NIT Warangal, India]
COMM_INTL_2:  [e.g. Dr. Rashmi Bhardwaj | Professor, GGSIPU, New Delhi, India]
COMM_INTL_3:  [e.g. Prof. Dr. Ismail Naci Cangul | Professor, Bursa Uludag University, Turkey]
COMM_INTL_4:  [e.g. Prof. Dafik | Professor & Dean, University of Jember, Indonesia]
COMM_INTL_5:  [e.g. Dr. Mansoor Saraj | Professor, Shahid Chamran University, Iran]
COMM_INTL_6:  [e.g. Dr. B. S. Panda | Professor, IIT Delhi, India]
COMM_INTL_7:  [e.g. Prof. Abdelmejid Bayad | Professor, Universite Paris-Saclay, France]
COMM_INTL_8:  [e.g. Dr. Ayman Badawi | Professor, American University of Sharjah, UAE]
# Add more by continuing the numbered list: COMM_INTL_9, COMM_INTL_10 ...


## ── SECTION 12: SPEAKERS ─────────────────────────────────────────────────
# Provide details for each confirmed speaker.
# IMAGE_FILE: filename only (e.g. S1.png) — must be placed in assets/img/speakers/
# If not yet confirmed, write: TBD for all fields of that speaker slot
# To have fewer than 8 speakers, write REMOVE for unused slots

SPEAKER_1_NAME:        [e.g. Prof. Yilmaz Simsek]
SPEAKER_1_DESIGNATION: [e.g. Professor, Department of Mathematics]
SPEAKER_1_INSTITUTION: [e.g. Akdeniz University, Antalya, Turkey]
SPEAKER_1_TOPIC:       [e.g. Special Functions & Combinatorial Mathematics]
SPEAKER_1_IMAGE_FILE:  [e.g. S1.png]

SPEAKER_2_NAME:        [e.g. Prof. Sivaramakrishnan Sivasubramanian]
SPEAKER_2_DESIGNATION: [e.g. Professor, Department of Mathematics]
SPEAKER_2_INSTITUTION: [e.g. IIT Bombay, Mumbai, India]
SPEAKER_2_TOPIC:       [e.g. Combinatorics & Algebraic Graph Theory]
SPEAKER_2_IMAGE_FILE:  [e.g. S2.png]

SPEAKER_3_NAME:        [e.g. Dr. Balaji Ramamurthy]
SPEAKER_3_DESIGNATION: [e.g. Professor, Department of Mathematics]
SPEAKER_3_INSTITUTION: [e.g. IIT Madras, Chennai, India]
SPEAKER_3_TOPIC:       [e.g. Applied & Computational Mathematics]
SPEAKER_3_IMAGE_FILE:  [e.g. S7.png]

SPEAKER_4_NAME:        [e.g. Dr. R. P. Suresh]
SPEAKER_4_DESIGNATION: [e.g. Professor, School of Computational & Data Sciences]
SPEAKER_4_INSTITUTION: [e.g. Vidyashilp University, India]
SPEAKER_4_TOPIC:       [e.g. Data Science & Computational Methods]
SPEAKER_4_IMAGE_FILE:  [e.g. S3.png]

SPEAKER_5_NAME:        [e.g. Prof. Ram Prakash Sharma]
SPEAKER_5_DESIGNATION: [e.g. Professor, Department of Mathematics]
SPEAKER_5_INSTITUTION: [e.g. NIT Arunachal Pradesh, India]
SPEAKER_5_TOPIC:       [e.g. Pure Mathematics & Algebra]
SPEAKER_5_IMAGE_FILE:  [e.g. S4.png]

SPEAKER_6_NAME:        [e.g. Prof. Srinivasa Rao Pentyala]
SPEAKER_6_DESIGNATION: [e.g. Professor, Department of Mathematics & Computing]
SPEAKER_6_INSTITUTION: [e.g. IIT (ISM) Dhanbad, Jharkhand, India]
SPEAKER_6_TOPIC:       [e.g. Mathematics & Computing]
SPEAKER_6_IMAGE_FILE:  [e.g. S6.png]

SPEAKER_7_NAME:        [e.g. Dr. Hari Ponnamma Rani]
SPEAKER_7_DESIGNATION: [e.g. Professor, Department of Mathematics]
SPEAKER_7_INSTITUTION: [e.g. NIT Warangal, Telangana, India]
SPEAKER_7_TOPIC:       [e.g. Fluid Mechanics & Heat Transfer]
SPEAKER_7_IMAGE_FILE:  [e.g. S5.png]

SPEAKER_8_NAME:        [e.g. Dr. Motahar Reza]
SPEAKER_8_DESIGNATION: [e.g. Associate Professor, Department of Mathematics]
SPEAKER_8_INSTITUTION: [e.g. GITAM Deemed University, Hyderabad, India]
SPEAKER_8_TOPIC:       [e.g. Computational & Applied Mathematics]
SPEAKER_8_IMAGE_FILE:  [e.g. S8.png]

# Add more speakers by copying the block above and numbering 9, 10, 11 ...


## ── SECTION 13: AGENDA / PROGRAMME ──────────────────────────────────────
# Format each item as: TIME | TITLE | DETAIL | TYPE
# TYPE options: session (normal) | break (tea/lunch/highlight)
# Leave as-is (copy from previous edition) if programme not yet finalised

# ---- DAY 1 ----
AGENDA_D1_TITLE:  [e.g. Day 1 — October 28, 2027]

AGENDA_D1_1: [08:30 - 09:00 | Registration & Welcome Kit Collection | Conference Registration Desk | break]
AGENDA_D1_2: [09:00 - 09:45 | Inaugural Ceremony | Welcome Address · Lamp Lighting · Address by the Vice Chancellor | session]
AGENDA_D1_3: [09:45 - 10:30 | Keynote Address — I | Speaker: To Be Announced | session]
AGENDA_D1_4: [10:30 - 11:15 | Keynote Address — II | Speaker: To Be Announced | session]
AGENDA_D1_5: [11:15 - 11:30 | Tea / Coffee Break & Networking | Conference Lounge | break]
AGENDA_D1_6: [11:30 - 13:00 | Oral Presentations — Session I | Fluid Dynamics · Graph Theory · Operations Research | session]
AGENDA_D1_7: [13:00 - 14:00 | Lunch Break | University Dining Hall | break]
AGENDA_D1_8: [14:00 - 15:30 | Oral Presentations — Session II | Algebra · Differential Equations · Geometry | session]
AGENDA_D1_9: [15:30 - 17:00 | Poster Presentations — Session I | Poster size: 90 cm (W) x 120 cm (H) | session]
AGENDA_D1_10:[17:00 - 17:30 | Evening Tea | Campus Grounds | break]

# Add more Day 1 items: AGENDA_D1_11, AGENDA_D1_12 ...

# ---- DAY 2 ----
AGENDA_D2_TITLE:  [e.g. Day 2 — October 29, 2027]

AGENDA_D2_1: [09:00 - 09:45 | Keynote Address — III | Speaker: To Be Announced | session]
AGENDA_D2_2: [09:45 - 10:30 | Invited Talk | Speaker: To Be Announced | session]
AGENDA_D2_3: [10:30 - 10:45 | Tea / Coffee Break | Conference Lounge | break]
AGENDA_D2_4: [10:45 - 12:30 | Oral Presentations — Session III | Complex Analysis · Number Theory · Numerical Analysis | session]
AGENDA_D2_5: [12:30 - 13:30 | Lunch Break | University Dining Hall | break]
AGENDA_D2_6: [13:30 - 15:00 | Oral Presentations — Session IV | Computational Fluid Mechanics · Mathematical Modelling | session]
AGENDA_D2_7: [15:00 - 16:00 | Poster Presentations — Session II | Fuzzy Logic & Applications · Mathematical Biology | session]
AGENDA_D2_8: [16:00 - 16:45 | Valedictory Ceremony & Best Paper Award | Certificates distributed to all participants | break]

# Add more Day 2 items: AGENDA_D2_9, AGENDA_D2_10 ...


## ── SECTION 14: THEMATIC AREAS ───────────────────────────────────────────
# List each thematic area on a new line prefixed with THEME:

THEME: Fluid Dynamics
THEME: Graph Theory
THEME: Operations Research
THEME: Geometry
THEME: Algebra
THEME: Differential Equations
THEME: Complex Analysis
THEME: Number Theory
THEME: Numerical Analysis
THEME: Computational Fluid Mechanics
THEME: Fuzzy Logic & Applications
THEME: Statistical Methods
THEME: Mathematical Modelling
THEME: Mathematical Biology
# Add or remove THEME lines as needed


## ── SECTION 15: CALL FOR ABSTRACT — SUBMISSION DETAILS ──────────────────

CFA_ABSTRACT_WORD_LIMIT:  [e.g. 250]
CFA_ORAL_SLOT_MINUTES:    [e.g. 15]
CFA_POSTER_SIZE:          [e.g. 90 cm (W) x 120 cm (H)]

# Deadline summary shown in CFA sidebar (mirrors Section 2 dates)
CFA_DEADLINE_REGISTRATION_OPEN:  [e.g. TBD]
CFA_DEADLINE_ABSTRACT:           [e.g. TBD]
CFA_DEADLINE_ACCEPTANCE:         [e.g. TBD]
CFA_DEADLINE_FULL_PAPER:         [e.g. TBD]
CFA_DEADLINE_LAST_REGISTRATION:  [e.g. TBD]
CFA_DEADLINE_CONFERENCE:         [e.g. Oct 28-29, 2027]


## ── SECTION 16: ANNOUNCEMENT TICKER ─────────────────────────────────────
# List each ticker item on a new TICKER_ITEM: line
# These scroll across the top of every page

TICKER_ITEM: Registration Opens: [date or Coming Soon]
TICKER_ITEM: Abstract Submission Deadline: [date or TBD]
TICKER_ITEM: Last Date for Registration: [date or TBD]
TICKER_ITEM: Confirmation of Accepted Abstracts: [date or TBD]
TICKER_ITEM: Conference Date: [display date]
TICKER_ITEM: Venue: School of Applied Sciences, REVA University, Bangalore
TICKER_ITEM: [Add any special announcement here — e.g. "Best Paper Award: Rs. 5,000"]
# Add or remove TICKER_ITEM lines as needed


## ── SECTION 17: ACCOMMODATION ────────────────────────────────────────────

HOSTEL_CONTACT_NAME:   [e.g. Dr. Udaya Kumara K. N.]
HOSTEL_CONTACT_PHONE:  [e.g. +91-9980923283]
HOSTEL_CONTACT_EMAIL:  [e.g. udayakumarkn@reva.edu.in]
HOSTEL_NOTE:           [e.g. On-site accommodation on a chargeable basis. Subject to availability.]


## ── SECTION 18: PAGE META (SEO) ──────────────────────────────────────────
# These are automatically derived from the above fields by the AI.
# Only fill in here if you want to override the auto-generated values.

META_TITLE_OVERRIDE:       [leave blank to auto-generate from CONFERENCE_ACRONYM + EDITION_NUMBER]
META_DESCRIPTION_OVERRIDE: [leave blank to auto-generate from conference name + venue + dates]


# ═══════════════════════════════════════════════════════════
# END OF INPUT DATA
# ═══════════════════════════════════════════════════════════

# After filling in the above, paste this entire file (with the HTML code
# at the top) into an AI assistant and request:
#
#   "Apply all the data from the INPUT section to the HTML code above
#    and return the complete updated index.html file."
#
# ═══════════════════════════════════════════════════════════
