<!--
DO NOT PUBLISH THIS VERSION YET. This branch must not be merged to main (main publishes
the live site) until BOTH of these are true:
  1. The "Sharing jobs to improve SlabIQ" section is ready to go live: the policy must be
     live BEFORE SLABIQ_CONTRIBUTIONS_ENABLED is turned on in production, and the
     contributions routes must be deployed with it.
  2. Every [CONFIRM n: ...] marker below is resolved and removed (see
     slabiq-app docs/SESSION_HANDOFF_2026-09-25.md section (d), and
     docs/CONTRIBUTIONS_2026-09-25.md).
Also check before publishing:
  - The app build with the one-time AI-processing prompt is live (the consent sentences
    below describe it).
  - Production runs Claude Opus 5.5 (the "About Anthropic" paragraph and "Finding the
    scale" describe the Opus 5.5 deploy). If production still runs Claude Fable 5, keep the
    live Fable 5 paragraph instead.
  - The docket and invoice reader (section 4) is described as if SLABIQ_DOCUMENTS_ENABLED
    is on. If it is still off when this publishes, that is harmless, but check the wording.
  - Set "Last updated" to the publish date.
Items marked [LAWYER] in HTML comments are for a solicitor if one is ever engaged.
-->

# SlabIQ Privacy Policy

**Last updated: 25 September 2026**

See also: [Terms of Use](https://mangomate.github.io/slabiq-privacy/terms/)

SlabIQ is an estimating app for Australian concreters. You give it a slab or
foundation plan, it reads the zones, dimensions and specifications, and it
turns them into a priced quote. This policy explains what information SlabIQ
handles, where it goes, how long it is kept, and the choices you have.

**The short version**

- SlabIQ has **no user accounts** and **no customer database**. Your quotes,
  clients, business details, price lists and job files stay **on your
  device**.
- The things that leave your device are the **plans you choose to scan**, any
  **job description** you type for a scan, **supplier price sheets you choose
  to import**, **delivery dockets and invoices you choose to scan**, and the
  **measurements and rates** needed to price a quote. Our server deletes them
  within about 30 minutes. We don't keep a library of your plans unless you
  turn on Sharing (see below).
- Plans, job descriptions, dockets and price sheets are read by AI models from
  **Anthropic** in the United States. Anthropic doesn't use them to train its
  models and keeps them for up to 30 days
  [CONFIRM 2: SlabIQ's Anthropic retention setting]. **We don't train AI
  models either.** If you choose to, you can share finished jobs with us to
  help us find and fix SlabIQ's mistakes; that's off unless you turn it on.
- The first time SlabIQ is about to send a file to the AI, the app asks for
  your OK. That one question covers plans, photos, price sheets, dockets and
  invoices, and Find Scale. If you say no, nothing is uploaded.
- Our server keeps a small amount of information about each install so it can
  enforce fair-use limits: a random identifier, this month's scan count and,
  on iPhone and iPad, a record of the device's Apple security key. It doesn't
  include your name, quotes or plans.
- Subscriptions are handled by **Apple / Google** and **RevenueCat**. We never
  see your card details.
- We do not sell your data, show ads, or use advertising or analytics
  trackers.

---

## Who we are

SlabIQ is developed and operated by Jake Murphy, a sole trader in Queensland,
Australia ("we", "us"). We handle personal information in line with the
*Privacy Act 1988* (Cth) and the Australian Privacy Principles.

SlabIQ doesn't use personal information to make automated decisions about
anyone.

Questions or requests: **slabiqapp@gmail.com**

---

## Information stored on your device

The following is saved in the app's own storage on your phone or tablet. It is
**not** sent to us, and we cannot access it:

- **Estimates and quotes**: project names, slab zones, dimensions, beam and
  footing details, quantities, rates, labour, extras and totals.
- **Client details**: client name, phone number, email address and site
  address.
- **Your business details**: business name, ABN and the bank details you add
  so they appear on your quotes and invoices.
- **Price lists and settings**: your material and labour rates, including
  rates you have imported from a supplier price sheet.
- **App housekeeping**: whether you have finished onboarding, how many free
  estimates and AI scans you have used this month, any extra scans you've
  bought, the last subscription level the store reported, whether you've
  agreed to AI processing, your Sharing choices, a random install identifier,
  and a short-lived access token. The token and, on iPhone and iPad, a
  reference to the app's Apple security key are kept in your device's secure
  storage (Keychain or Android Keystore).
- **The last crash report**, if the app has crashed (see "Crash reports").

Quote PDFs are generated on your device. When you share or email a quote, the
app hands it to your device's share sheet or email app. What happens next is
up to you and the app you choose.

**Plan and docket files on your phone.** SlabIQ keeps the plan files, page
images and docket or invoice photos for each job in its own storage on your
phone until you delete the job or use Backups → Remove files. They're not in
backup exports and never leave your phone except when you scan them or share
the job with us.

**Backups.** You can export a backup of your saved estimates, including client
details and invoices, as a file. The app hands it to your share sheet; what
happens next is up to you. The app tidies up its own copies of backup files
older than about a day the next time you export. Your phone's own backup
(iCloud or Google) may also include SlabIQ's saved estimates, under your
device settings.

---

## Information that leaves your device

### 1. Plans you scan

When you use the plan reader, the PDF pages or photos you choose are uploaded
over an encrypted (HTTPS) connection to our processing server. The server:

- extracts text, dimensions and schedules from the drawing with its own
  software, and
- sends the plan, and the page images it renders from it, to **Anthropic's
  Claude AI API** to identify slab zones, dimensions, beams and
  specifications.

Plans often contain other people's personal information, such as the property
owner's name, the site address, or the designer's and engineer's details. We
don't look for or pull out that information. Please upload only plans you are
allowed to share for pricing a job.

The first time SlabIQ is about to send a file to our AI provider, the app asks
for your OK. That one question covers plans, photos, price sheets, dockets and
invoices, and Find Scale. If you say no, nothing is uploaded, and you can
still build estimates by entering measurements manually.

**Finding the scale.** When you use Find Scale on a PDF plan, the server first
looks for the printed scale in the drawing's text. If it can't find one, it
sends an image of that one page to Anthropic to read the printed scale. This
doesn't use a monthly scan. Photos are never sent for this.

**Retention:** files written to the server during a scan are deleted when the
scan finishes. So that a multi-step scan doesn't need the same plan uploaded
twice, an uploaded PDF may be held in a temporary cache for **up to about 30
minutes**, then it is deleted. We do not keep copies of your plans unless you
share the job with us (see "Sharing jobs to improve SlabIQ").

### 2. Job descriptions

When you scan a plan you can type a short description of the actual job, such
as "garage slab only". This text is sent with the plan to Anthropic so the AI
can focus on the right scope. It is not stored on our server, and it is never
included in jobs you share with us.

### 3. Supplier price sheets

When you import a supplier price list spreadsheet, the file is sent
to our server. It is converted to text there and sent to Anthropic, which
matches the supplier's prices to the app's price fields and double-checks
them. The file isn't stored. Our server log records only that an import
happened, with the install identifier, the file size and how many prices were
matched.

### 4. Delivery dockets and invoices

When you scan concrete delivery dockets or a supplier's invoice, the photos or
PDF you choose are sent to our server and on to Anthropic, which reads what
was delivered and the prices charged. The app shows you any price changes to
accept or reject; nothing changes on its own. The files are held only in the
server's memory while they are read (a PDF is briefly written to a private
folder and deleted when the read finishes). Our server log records only
counts, such as how many files and pages there were, never the supplier,
amounts or what the documents say.

### 5. Quote calculations

To price a quote, the app sends the slab measurements and your rates (zones,
waste percentage, material and labour prices, extras) to our server's
calculation engine. **No client contact details or bank details are sent**,
though zone names and any notes you type into the measurements are. This step
doesn't use AI, and nothing is stored.

### 6. Install identifier and device security

SlabIQ doesn't use accounts. Instead, each install gets a random identifier.
On iPhone and iPad, the app also creates a security key with Apple's App
Attest, and our server gives that install its own random identifier. On
Android, the app creates the random identifier itself. The identifier isn't
your name, email or phone number. The app swaps it for a short-lived access
token (15 minutes to 24 hours).

We use the identifier only to:

- enforce fair-use limits (scans per month and requests per hour),
- protect the service from abuse and runaway costs,
- check your subscription with RevenueCat (see section 9),
- link the jobs you share with us to your install, so you can see and delete
  them (see "Sharing jobs to improve SlabIQ"), and
- link a crash or error report to a single install when we are
  troubleshooting.

**What our server stores.** Our server keeps a small database on our hosting
provider's storage:

- for iPhone and iPad installs: the security key's ID and public key, the
  random identifier, when it was set up, the app version, and a counter Apple
  uses to stop replayed requests. These are kept while SlabIQ runs so we can
  recognise the device.
  [CONFIRM 4: retention period for device records, and deletion on request]
- the number of AI scans each identifier has used this month (earlier months
  are deleted), and
- the total AI cost for the whole service each day (not per person), kept for
  about 13 months.

Hourly request limits are kept only in the server's memory.

Deleting the app removes the identifier stored in the app. On iPhone and iPad,
the device's secure storage may keep the security key after the app is
deleted. The records on our server stay until they are removed as described
above or you ask us to delete them.

### 7. Crash reports

If the app crashes, it saves a short report on your device and sends a copy
to our server: the error message, the technical stack trace, your platform
(iOS or Android), the time, and your install identifier. It is designed not
to include your quotes, client details or plans, but an error message can
occasionally include text that was on screen. Crash reports go into our
hosting provider's logs so we can fix bugs.
[CONFIRM 5: how long Railway keeps logs on SlabIQ's plan]

### 8. Technical data

Like any internet service, our server and its hosting provider see technical
information about each request, such as your IP address and the time of the
request. We use your IP address, in memory only, for rate limiting and abuse
protection. Our hosting provider may keep standard request logs under its own
policies.

### 9. Subscriptions and payments

SlabIQ has a free tier and paid subscriptions. Purchases are processed by
**Apple (App Store)** or **Google (Play Store)**, and we never receive your
payment card details. Subscription status is managed by **RevenueCat**, which
receives your install identifier (see section 6), your purchase and
subscription history, and basic device and app information such as platform
and app version. Our server may check your subscription status with
RevenueCat, using that identifier, to decide which usage limits apply to you.
[CONFIRM 6: are subscriptions live? If not, say "Paid subscriptions are coming
soon".]

### 10. Camera and photos

SlabIQ asks for camera access **only** so you can photograph a plan, docket or
invoice. On iPhone and iPad it also asks for photo library access so you can
pick a saved image; on Android you pick an image with the system picker, which
doesn't give SlabIQ access to your whole library. It doesn't read your photos
in any other way. You can turn these permissions off at any time in your
device settings.

---

## Sharing jobs to improve SlabIQ (optional)

<!-- [LAWYER] This section describes a secondary purpose (APP 6) that relies on express,
opt-in consent given in the app. Confirm the wording is adequate notice under APP 5 and
that the "averages can't be taken back" and "reviewed examples stay in our test set"
statements are acceptable. -->

If you turn on **Sharing**, the app sends us finished jobs so we can find where
SlabIQ reads plans wrongly and fix it. You choose what to share: (a) plans and
what the AI read from them; (b) delivery dockets and invoices; (c) your
corrections, pour totals and rates, with no files.

**What we do with it:** we compare what the AI read with what you corrected,
use the examples to test changes to our plan-reading prompts and rules, and
work out averages such as waste by slab type or typical rates by state, from
many jobs together.

**What we don't do:** we don't sell or publish your jobs, don't show them to
other users, don't use them to train Anthropic's or anyone else's AI models,
and don't use them for anything except improving SlabIQ. We don't pay or
reward you for sharing.

**Before we keep a plan or docket** we remove the file's hidden metadata and
black out the names, addresses and phone numbers we can find in the title
block. Zone names and your rates are included; your client's contact details,
your bank details, notes and invoices you issue are never sent. We also
receive the job's state (such as QLD), so we can compare rates by state.

**How long:** up to 24 months on our server, then deleted; a small number of
reviewed examples stay in our private test set while we run SlabIQ, unless you
withdraw.

**Stopping:** turn a switch off or tap "Delete everything I've shared". Your
shared jobs are deleted from our server straight away and from our review
copies within 30 days. Averages we've already worked out from many jobs can't
be taken back. You can also stop any single job from being shared with
"Don't share this job".

Shared jobs are stored encrypted with our hosting provider
[CONFIRM 3: Railway region], and every access is logged. They're linked to
your install identifier, not to your name.

---

## Who we share information with

We share information only with the service providers SlabIQ needs in order to
work:

| Provider | What they receive | Why |
|---|---|---|
| **Anthropic** (Claude API) | Plans and rendered page images, job descriptions, price sheet contents, docket and invoice images, single pages for Find Scale | AI reading of plans, scales, price sheets, dockets and invoices (retention: see below) |
| **Railway** | Everything sent to our server while it is processed; the small install database in section 6; jobs you choose to share (encrypted); server logs | Hosting our server [CONFIRM 3: Railway region] |
| **RevenueCat** | Install identifier, purchase history, device/app info | Managing subscriptions |
| **Apple / Google** | Purchase and payment details | Billing, under their own terms |

**About Anthropic.** Anthropic's
[Commercial Terms](https://www.anthropic.com/legal/commercial-terms) state
that it "may not train models on Customer Content" sent through its API.
SlabIQ reads plans and scales with Claude Opus 5.5; page ranking uses Claude
Sonnet 5, and price sheets, dockets and invoices are read with Claude Sonnet 5
and Claude Haiku 4.5. Anthropic keeps what we send for up to 30 days, longer
only if its automated safety systems flag a request, in which case it may keep
that request for up to 2 years.
[CONFIRM 2: whether SlabIQ's Anthropic organisation has a 30-day default
retention, and that no setting switches back to a Covered Model]
Details:
[API and data retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention).

RevenueCat's policy is at [revenuecat.com/privacy](https://www.revenuecat.com/privacy).

We do not sell or rent personal information, and we don't share it for
advertising.

### Overseas processing

Our server and our providers may process information **outside Australia**,
mainly in the **United States**. We use established providers that have their
own security and privacy commitments. By using the plan reader, Find Scale,
price-sheet import or the docket reader, you understand that the files you
choose will be processed overseas. Jobs you share with us are stored outside
Australia too. [CONFIRM 3: Railway region]

---

## Security

All communication between the app and our server is encrypted with HTTPS. Our
AI features need an access token issued to each install; on iPhone and iPad
that token is only issued to a genuine copy of the app, checked with Apple's
App Attest. They're also protected by rate limits, usage quotas and a daily
spending cap. Plan files are held only as long as processing needs them,
unless you share the job with us, in which case they're stored encrypted.

Data on your device is protected by your device's own security, such as your
passcode and encryption. No system is perfectly secure. If you're not
comfortable with a document being processed by a third-party AI service,
please don't upload it.

---

## Your choices and rights

- **Your on-device data:** you can edit or delete estimates, clients and
  business details in the app. Uninstalling SlabIQ deletes its local data,
  but not backup files you've exported or shared, copies in your phone's own
  backup, or (on iPhone and iPad) its security key in secure storage.
- **Server-side data:** we don't keep an account or profile about you. The
  only records linked to an install are the small database described in
  section 6, jobs you choose to share, and short technical logs (such as crash
  and error lines). In Sharing you can see how many jobs and files you've
  shared and delete them yourself. To ask what we hold or ask us to delete it,
  email **slabiqapp@gmail.com**, including your install identifier if you can.
  [CONFIRM 7: how Jake will look up and delete an install's device rows]
- **Subscriptions:** you can manage or cancel your subscription in your App
  Store or Google Play account settings. For data RevenueCat holds, you can
  also contact RevenueCat directly.
- **Complaints:** if you have a privacy concern, please contact us first and
  we'll respond within 30 days. If you're not satisfied with our response, you
  can complain to the Office of the Australian Information Commissioner at
  [oaic.gov.au](https://www.oaic.gov.au).

---

## Children

SlabIQ is a business tool for people working in the construction industry. It
is not directed at children, and we don't knowingly collect information from
anyone under 18.

---

## Changes to this policy

SlabIQ is under active development, so this policy will change as the app
does. When it changes we will update the "Last updated" date above. If a
change is significant, such as keeping plans for longer or using them for a
new purpose, we will tell you in the app **before** it takes effect, and we
will ask for your consent where the law requires it.

---

## Contact

**Jake Murphy**, SlabIQ
Queensland, Australia
slabiqapp@gmail.com

---

*SlabIQ is not affiliated with Apple Inc., Google LLC, Anthropic PBC, Railway
Corp. or RevenueCat, Inc.*
