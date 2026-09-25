# SlabIQ Privacy Policy

**Last updated: 26 September 2026**

See also: [Terms of Use](https://mangomate.github.io/slabiq-privacy/terms/)

SlabIQ is an estimating app for Australian concreters. You give it a slab or
foundation plan, it reads the zones, dimensions and specifications, and it
turns them into a priced quote. This policy explains what information SlabIQ
handles, where it goes, how long it is kept, and the choices you have.

**The short version**

- SlabIQ has **no user accounts**. Your quotes, clients, business details and
  price lists stay **on your device**.
- The things that leave your device are the **plans you choose to scan**, any
  **job description** you type for a scan, **supplier price sheets you choose
  to import**, and the **measurements and rates** needed to price a quote.
  Our server deletes uploaded files within about 30 minutes. It keeps a
  recovery copy of each scan's result for 24 hours, in case your connection
  drops. We don't keep a library of your plans.
- Plans, job descriptions and price sheets are read by AI models provided by
  **Anthropic**, in the United States. Neither we nor Anthropic use them to
  train AI models. Anthropic keeps them for up to 30 days, depending on the
  model, or up to 2 years if its safety systems flag a request (see "About
  Anthropic" below).
- The app asks for your OK before anything is sent to the AI. If you say no,
  nothing is sent, and you can still build estimates by entering measurements
  yourself.
- Our server keeps a small amount of information about each install so it can
  count scans and enforce fair-use limits: a random identifier, records of
  recent scans (with a fingerprint of each plan file, not the plan itself), a
  short-lived daily usage record and, on iPhone and iPad, a record of the
  device's Apple security key. It doesn't include your name, your quotes or
  your plans. See "How long we keep information".
- You can ask us to delete what our server holds about your install from the
  app's **Your data** section.
- Paid subscriptions are coming soon. They will be handled by **Apple /
  Google** and **RevenueCat**. We never see your card details.
- We do not sell your data, show ads, or use advertising or analytics
  trackers.

---

## Who we are

SlabIQ is developed and operated by Jake Murphy, a sole trader in Queensland,
Australia ("we", "us"). We are an Australian business, and we handle personal
information in line with the *Privacy Act 1988* (Cth) and the Australian
Privacy Principles (APPs).

You don't have to give us your name or contact details to use SlabIQ. We only
learn them if you email us.

Questions or requests: **slabiqapp@gmail.com**

---

## Information stored on your device

The following is saved in the app's own storage on your phone or tablet. It
stays there unless a feature described under "Information that leaves your
device" sends part of it (for example, measurements for a price calculation).
We can't access your device.

- **Estimates and quotes**: project names, slab zones, dimensions, beam and
  footing details, quantities, rates, labour, extras, markup, totals and
  invoices.
- **Client details**: client name, phone number, email address and site
  address.
- **Your business details**: business name, ABN and the bank details you add
  so they appear on your quotes and invoices.
- **Price lists and settings**: your material and labour rates, including
  rates you have imported from a supplier price sheet, and any zone templates
  you save.
- **App housekeeping**: whether you have finished onboarding and whether you
  have agreed to AI sharing, how many of your 3 free estimates you have used
  (3 in total, not per month), how many AI scans you have used this month,
  fingerprints of the plan files you've scanned (so the app knows which
  re-scans are free), a history of how long your scans took (so it can
  estimate waiting times), any extra scans you've bought, the last
  subscription level the store reported, a random install identifier, and a
  short-lived access token. The token and, on iPhone and iPad, a reference to
  the app's Apple security key are kept in your device's secure storage
  (Keychain or Android Keystore).
- **The last crash report**, if the app has crashed (see "Crash reports").

Quote PDFs are generated on your device. When you share or email a quote, the
app hands it to your device's share sheet or email app. What happens next is
up to you and the app you choose.

**Backups.** You can export a backup of your saved estimates, including client
details and invoices, as a file. The app hands it to your share sheet; what
happens next is up to you. The app tidies up its own copies of backup files
older than about a day the next time you export. Your phone's own backup
(iCloud or Google) may also include SlabIQ's saved estimates, depending on
your device settings.

---

## Information that leaves your device

Unless a section says otherwise, everything below is sent over an encrypted
(HTTPS) connection to our server, which runs on our hosting provider, Railway.

### Your OK comes first

The first time you open SlabIQ, the last welcome screen explains what is sent
to our AI provider and asks for your OK. If you were already using SlabIQ
before this screen was added, the app asks once, the next time you open it.

- If you choose **I agree**, the app remembers your answer on your device.
  Nothing is sent until you choose to scan a plan, find a scale or import a
  price sheet.
- If you choose **Not now**, nothing is sent. The AI features ask again at the
  moment you use them.
- **Nothing is sent to the AI without your OK.** Manual estimating works
  without it.

### 1. Plans you scan

When you use the plan reader, the PDF pages or photos you choose are uploaded
to our server. The server:

- extracts text, dimensions and schedules from the drawing with its own
  software,
- for a PDF with several pages, may send pictures of the pages to the AI to
  work out which one shows the slab (a page preview), and
- sends the plan, and the page images it renders from it, to **Anthropic's
  Claude AI** to identify slab zones, dimensions, beams and specifications.

Plans often contain other people's personal information, such as the property
owner's name, the site address, or the designer's and engineer's details. We
don't look for or pull out that information. Please upload only plans you are
allowed to share for pricing a job.

**Finding the scale.** When you use Find Scale on a PDF plan, the server first
looks for the printed scale in the drawing's text. If it can't find one, it
sends an image of that one page to Anthropic to read the printed scale. This
doesn't use a scan from your allowance, though Find Scale reads are counted
towards a daily limit (see section 6). Photos are never sent for this.

**How long:** files written to the server during a scan are deleted when the
scan finishes. So that a multi-step scan doesn't need the same plan uploaded
twice, an uploaded file may be held in a temporary cache for **up to about 30
minutes**, then it is deleted. We don't keep copies of your plans.

So that a dropped connection doesn't lose a finished scan, the server keeps a
**recovery copy of the scan's result for 24 hours**: the zones, measurements
and text the AI read from the plan, including a picture of the plan page. It
is used only to give the result back to you. It is deleted after 24 hours (in
practice, within about 25 hours, because the clean-up runs on a schedule).

### 2. Job descriptions

When you scan a plan you can type a short description of the actual job, such
as "garage slab only". This text is sent with the plan to Anthropic so the AI
can focus on the right scope. Our server doesn't store the description text
itself. The 24-hour recovery copy of a scan's result (see section 1) can
include the AI's notes, which may mention your description. Section 6
describes the fingerprint the server keeps.

### 3. Supplier price sheets

When you import a supplier price list spreadsheet, the file is sent to our
server. It is converted to text there and sent to Anthropic, which matches the
supplier's prices to the app's price fields and double-checks them. The file
isn't stored, and an import doesn't use a scan from your allowance. Our server
log records only that an import happened, with the install identifier, the
file size and how many prices were matched.

### 4. Quote calculations

To price a quote, the app sends the slab measurements and your rates (zones,
waste percentage, material and labour prices, extras) to our server's
calculation engine. **No client contact details or bank details are sent**,
though zone names and any notes you type into the measurements are. This step
doesn't use AI, and nothing is stored.

### 5. Install identifier and device security

SlabIQ doesn't use accounts. Instead, each install gets a random identifier.
On iPhone and iPad, the app also creates a security key with Apple's App
Attest, and our server gives that install its own random identifier. On
Android, the app creates the random identifier itself. The identifier isn't
your name, email or phone number. The app swaps it for a short-lived access
token (15 minutes to 24 hours).

We use the identifier only to:

- count your scans and enforce fair-use limits (see section 6),
- protect the service from abuse and runaway costs,
- check your subscription with RevenueCat, once paid subscriptions launch (see
  section 9), and
- link a crash or error report to a single install when we are
  troubleshooting.

**Device security record.** For iPhone and iPad installs, our server keeps the
security key's ID and public key, the random identifier, when it was set up,
the day it was last used, the app version, Apple's validation category for
the device, whether the record has been revoked, and a counter Apple uses to
stop replayed requests. It also keeps one-time security challenges, which
expire after a few minutes. We keep the record while you use SlabIQ, so we can
recognise a genuine copy of the app on your device, and delete it after 12
months without use.

Deleting the app removes the identifier stored in the app. On iPhone and iPad,
the device's secure storage may keep the security key after the app is
deleted. The records on our server stay until they are removed on the schedule
in "How long we keep information", or until you ask us to delete them.

### 6. Scan records and fair-use limits

**What counts as a scan.** One plan successfully processed is one scan. Reads
that don't produce a usable result (for any reason), page previews, Find
Scale and price-sheet imports don't count. Re-scanning the same plan page in
the same estimate is free if you scanned that estimate this month or in
either of the previous two calendar months (UTC). A different page or a
different plan file counts as a new scan. Editing the job description
doesn't.

**Scan records.** To count scans against your monthly allowance, give you free
re-scans of the same plan, and answer billing questions, our server keeps a
record of each AI plan scan, linked to your install identifier:

- which estimate was scanned (the app's reference number for it, not its name
  or contents);
- a fingerprint of what you scanned (the plan file, the page and any job
  description). A fingerprint is a short code worked out from the file. It
  lets us recognise the same plan again, but the plan can't be rebuilt from
  it; and
- when the scan happened, whether it succeeded, which AI model read it, and
  what the read cost us.

Scan records linked to your install are kept until the end of the second
calendar month (UTC) after that estimate's last scan, so free re-scans keep
working, then de-identified: we keep only monthly cost totals, with no
install, estimate or plan information, for 5 years. If our server restarts in
the middle of a scan, the unfinished scan is released without charge within
about 10 days.

**Daily usage record.** Every install that uses AI features has a small usage
record, kept for about 2 days. It holds this day's count of failed reads, this
day's count of scans stopped before they finish, the estimated AI cost of
your reads that day, your Find Scale reads that day, and any cooldown that
applies.

A read counts as failed if it finishes but its result can't be used
(including when the AI declines the plan or its answer is cut off or
unreadable). Scans stopped before they finish — because you cancelled, the
connection dropped or our time limit was reached — are counted separately,
with a higher daily limit. Errors on the AI provider's side, including a
provider response that ends early, don't count against you, though their AI
cost still counts toward the daily usage limit, as every read's cost does.

**Plans that keep failing.** If a plan's result can't be used, the server keeps
a fingerprint of that plan file (not the plan) for about 2 days, so the same
plan can't be read again and again while it keeps failing.

**Per-network counters.** Some limits apply to each internet connection. For
these, the server keeps counters under a keyed one-way hash of your IP
address, for about 2 days. A keyed hash is a scrambled code: the address
can't be read back from it, but the same address always gives the same code,
so while it is kept it still relates to your connection. It isn't anonymous.

**Other limits.** The server also keeps:

- this month's count of scans and AI read attempts for each install, for the
  current month only;
- hourly request limits, in the server's memory; and
- the total AI cost for the whole service each day, which isn't about any
  person, kept for about 13 months.

### 7. Crash reports

If the app crashes, it saves a short report on your device and sends a copy to
our server: the error message, the technical stack trace, your platform (iOS
or Android), the time, and your install identifier. It is designed not to
include your quotes, client details or plans, but an error message can
occasionally include text that was on screen. Crash reports go into our
hosting provider's logs so we can fix bugs.

### 8. Technical data

Like any internet service, our server and its hosting provider see technical
information about each request, such as your IP address and the time of the
request. We use your IP address for rate limiting and abuse protection: in the
server's memory for hourly limits, and as a keyed one-way hash in the
per-network counters described in section 6 (kept for about 2 days). Our
hosting provider keeps standard request logs under its own policies.

### 9. Subscriptions and payments

**Paid subscriptions are coming soon.** SlabIQ will have a free tier and paid
plans (see the [Terms of Use](https://mangomate.github.io/slabiq-privacy/terms/)).
When they launch:

- Purchases will be processed by **Apple (App Store)** or **Google (Play
  Store)**. We never receive your payment card details.
- Subscription status will be managed by **RevenueCat**, which will receive
  your install identifier (see section 5), your purchase and subscription
  history, and basic device and app information such as platform and app
  version.
- Our server may check your subscription status with RevenueCat, using that
  identifier, to decide which plan's limits apply to you.
- If a subscription can be shared across your devices (this isn't live yet),
  we keep the store purchase-lineage records needed to apply it to each
  device. They are kept for up to 5 years, and deleted with your install
  unless the subscription is shared with another of your devices.

### 10. Camera and photos

SlabIQ asks for camera access **only** so you can photograph a plan. On iPhone
and iPad it also asks for photo library access so you can pick a saved plan
image; on Android you pick an image with the system picker, which doesn't give
SlabIQ access to your whole library. It doesn't read your photos in any other
way. You can turn these permissions off at any time in your device settings.

---

## How long we keep information

- **Uploaded plans, photos and price sheets** (our server): only while they
  are being processed, and deleted within about 30 minutes. *Why:* to read
  them.
- **Recovery copy of a scan result**, including a picture of the plan page
  (our server): deleted after 24 hours (in practice, within about 25 hours).
  *Why:* so a dropped connection can recover the result.
- **Scan records linked to your install** (our server): until the end of the
  second calendar month (UTC) after that estimate's last scan, then
  de-identified.
  They say which estimates were scanned, with a fingerprint of the plan file
  (not the plan itself) and the AI cost. *Why:* your scan allowance, free
  re-scans and billing questions. If our server restarts in the middle of a
  scan, the unfinished scan is released without charge within about 10
  days.
- **De-identified AI cost records** (our server): kept only as monthly totals,
  with no install, estimate or plan information, for 5 years, then deleted.
  *Why:* business and tax record-keeping.
- **Daily usage record** (our server): about 2 days. It holds the day's counts
  of failed reads and of scans stopped before they finish, estimated AI usage
  cost, Find Scale reads and any cooldown. *Why:* daily fair-use limits and
  abuse protection.
- **Fingerprints of plans whose result couldn't be used** (our server): about
  2 days. *Why:* to stop the same failing plan being read again and again.
- **Per-network counters**, under a keyed one-way hash of your IP address
  (our server): about 2 days. *Why:* limits for each internet connection.
- **This month's scan and AI read attempt counts** (our server): the current
  month only. *Why:* fair-use limits.
- **iPhone and iPad device security record** (our server): while you use
  SlabIQ, and deleted after 12 months without use. *Why:* to recognise a
  genuine copy of the app on your device.
- **Service-wide daily AI cost totals** (our server, not about any person):
  about 13 months. *Why:* the daily spending cap and tracking our costs.
- **Server logs and crash reports** (our hosting provider): for our hosting
  provider's log-retention period. <!-- CONFIRM: Railway log retention -->
  *Why:* fixing bugs and keeping the service secure.
- **Copies at Anthropic**: up to 30 days depending on the model, or up to 2
  years if Anthropic's safety systems flag a request (see "About Anthropic").
  *Why:* Anthropic's own misuse and safety monitoring.
- **Store purchase-lineage records** (our server, only if subscriptions are
  shared across devices, which isn't live yet): up to 5 years, and deleted
  with your install unless the subscription is shared with another of your
  devices. *Why:* to apply your subscription to each of your devices.
- **Purchase records** (Apple, Google and RevenueCat, once paid subscriptions
  launch): under their own policies.
- **Everything on your device**: until you delete it or uninstall the app.
  Backups you export, and your phone's own backups, are yours to keep or
  delete.

---

## Who we share information with

We share information only with the service providers SlabIQ needs in order to
work:

| Provider | What it receives | Why |
|---|---|---|
| **Anthropic** (Claude API) | Plans and rendered page images, job descriptions, price sheet contents, single pages for Find Scale | AI reading of plans, scales and price sheets (retention: see below) |
| **Railway** | Everything sent to our server while it is processed; the server records described in sections 1, 5 and 6; server logs | Hosting our server |
| **RevenueCat** (once paid subscriptions launch) | Install identifier, purchase history, device/app info | Managing subscriptions |
| **Apple / Google** (once paid subscriptions launch) | Purchase and payment details | Billing, under their own terms |

**About Anthropic.** Anthropic's
[Commercial Terms](https://www.anthropic.com/legal/commercial-terms) state
that it "may not train models on Customer Content" sent through its API.
SlabIQ reads plans and finds scales with Claude Opus 5.5. Page previews
(working out which page shows the slab) use Claude Sonnet 5, and price-sheet
reading uses Claude Sonnet 5 and Claude Haiku 4.5. If one of these models is
busy, the request may be passed to another Claude model.

Anthropic keeps what we send for **up to 30 days, depending on the model**,
then deletes it. Anthropic's current documentation says it doesn't keep
prompts and outputs for most models by default, but keeps them for 30 days
for a group of "Covered Models" (such as Claude Fable 5), to detect misuse. We
may sometimes switch plan reading back to a Covered Model for a while, for
example if another model has problems. If Anthropic's automated safety systems
flag a request, it may keep that request for up to 2 years. Details:
[API and data retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention).

RevenueCat's policy is at [revenuecat.com/privacy](https://www.revenuecat.com/privacy).

We do not sell or rent personal information, and we don't share it for
advertising.

### Overseas processing

Some information is sent to, and processed by, providers outside Australia:

- **Anthropic** processes plans, page images, job descriptions and price
  sheets in the **United States**.
- **Railway**, our hosting provider, runs our server and holds its records and
  logs outside Australia, mainly in the **United States**.
  <!-- CONFIRM: Railway region -->
- **RevenueCat, Apple and Google** (once paid subscriptions launch) may process
  purchase and subscription information in the United States and other
  countries.

We use established providers that have their own security and privacy
commitments, and we send them only what they need to do their job. By using
the plan reader, Find Scale or price-sheet import, you understand that the
files you choose will be processed overseas.

---

## Security

All communication between the app and our server is encrypted with HTTPS. Our
AI features need an access token issued to each install; on iPhone and iPad
that token is only issued to a genuine copy of the app, checked with Apple's
App Attest. They're also protected by rate limits, usage quotas and a daily
spending cap. Plan files are held only as long as processing needs them.

Data on your device is protected by your device's own security, such as your
passcode and encryption. No system is perfectly secure. If you're not
comfortable with a document being processed by a third-party AI service,
please don't upload it.

---

## Your choices and rights

### Your on-device data

You can edit or delete estimates, clients and business details in the app.
Uninstalling SlabIQ deletes its local data, but not backup files you've
exported or shared, copies in your phone's own backup, or (on iPhone and iPad)
its security key in secure storage.

### Asking us to delete server data

We don't keep an account or profile about you. To ask us to delete what our
server holds about your install, open the **Your data** section in SlabIQ. It
shows your install identifier and has a **Request data deletion** button,
which starts an email to **slabiqapp@gmail.com**. Make sure the email includes
the install identifier shown in that section, so we can find your records.
You can also email us directly.

We'll respond within 30 days, and we'll email you exactly what we deleted,
what we kept and why.

**What we delete:** your device security record, your scan and attempt
counts, your daily usage record, your scan records and the plan fingerprints
linked to your install, any recovery copies of your scan results, any store
purchase-lineage records for your install, and the link between your install
and any other records.

If a subscription is shared with another of your devices (this isn't live
yet), the scan records, recovery copies and purchase-lineage records that
belong to that shared subscription are kept for the other device.

**What we keep, and why:**

- **De-identified AI cost records**: monthly cost totals with no install,
  estimate or plan information, kept for 5 years for business and tax
  record-keeping.
- **Service-wide daily totals**, which aren't about any person.
- **Server logs**, which carry your install identifier (for example, crash
  reports and error lines), until they expire under our hosting provider's
  retention period.
- **Per-network counters**, which are kept under a hashed IP address rather
  than your install identifier, until they expire after about 2 days.
- **Copies at Anthropic**, which Anthropic deletes under its own retention
  (see "About Anthropic").
- **Purchase records** that Apple, Google and RevenueCat hold under their own
  policies. You can also contact RevenueCat directly about data it holds.

**If you've reinstalled SlabIQ** or moved to a new phone, the identifier the
app shows now may be a new one. Records made under an earlier identifier can
only be found with that identifier. If you no longer have it, those records
are still removed or de-identified on the schedule in "How long we keep
information".

After a deletion, SlabIQ may need to set up its connection to our server again
the next time you use an online feature.

### Access and correction

You can ask for a copy of the personal information we hold about you, and ask
us to correct it if it's wrong, out of date or incomplete. Email
**slabiqapp@gmail.com**, including your install identifier if you can. We'll
respond within 30 days, and there's no charge to make a request. Because
SlabIQ has no accounts, we may ask for your install identifier or other
details to check the records are yours before we share them. If we can't do
what you ask, we'll tell you why in writing and how you can complain.

### Subscriptions

Once paid subscriptions launch, you can manage or cancel your subscription in
your App Store or Google Play account settings. For data RevenueCat holds, you
can also contact RevenueCat directly.

### Complaints

If you have a privacy concern, or think we haven't handled your information
in line with the Australian Privacy Principles, please contact us first at
**slabiqapp@gmail.com**. We'll respond within 30 days. If you're not satisfied
with our response, you can complain to the Office of the Australian
Information Commissioner (OAIC) at [oaic.gov.au](https://www.oaic.gov.au) or on
1300 363 992.

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
