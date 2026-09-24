# SlabIQ Privacy Policy

**Last updated: 24 September 2026**

SlabIQ is an estimating app for Australian concreters. You give it a slab or
foundation plan, it reads the zones, dimensions and specifications, and it
turns them into a priced quote. This policy explains what information SlabIQ
handles, where it goes, how long it is kept, and the choices you have.

**The short version**

- SlabIQ has **no user accounts** and **no customer database**. Your quotes,
  clients, business details and price lists stay **on your device**.
- The things that leave your device are the **plans you choose to scan**, any
  **job description** you type for a scan, **supplier price sheets you choose
  to import**, and the **measurements and rates** needed to price a quote.
  Our server deletes them within about 30 minutes. We don't keep a library
  of your plans.
- Plans, job descriptions and price sheets are read by AI models provided by
  **Anthropic**. Neither we nor Anthropic use them to train AI models.
  Anthropic keeps them for up to 30 days for safety monitoring, then deletes
  them.
- The app asks for your OK before it sends any file to the AI for the first
  time.
- Subscriptions are handled by **Apple / Google** and **RevenueCat**. We never
  see your card details.
- We do not sell your data, show ads, or use advertising or analytics
  trackers.

---

## Who we are

SlabIQ is developed and operated by Jake Murphy, a sole trader in Queensland,
Australia ("we", "us"). We handle personal information in line with the
*Privacy Act 1988* (Cth) and the Australian Privacy Principles.

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
  estimates you have used, a short-lived access token, and a random install
  identifier (explained below).
- **The last crash report**, if the app has crashed (see "Crash reports").

Quote PDFs are generated on your device. When you share or email a quote, the
app hands it to your device's share sheet or email app. What happens next is
up to you and the app you choose.

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

Before the first plan or price sheet is sent, the app asks for your
permission to share it with our AI provider. You can say no, and nothing is
uploaded. You can still build estimates by entering measurements manually.

**Retention:** files written to the server during a scan are deleted when the
scan finishes. So that a multi-step scan doesn't need the same plan uploaded
twice, an uploaded PDF may be held in a temporary cache for **up to about 30
minutes**, then it is deleted. We do not keep copies of your plans.

### 2. Job descriptions

When you scan a plan you can type a short description of the actual job, such
as "garage slab only". This text is sent with the plan to Anthropic so the AI
can focus on the right scope. It is not stored on our server.

### 3. Supplier price sheets

When you import a supplier price list spreadsheet, the file is sent
to our server. It is converted to text there and sent to Anthropic, which
matches the supplier's prices to the app's price fields and double-checks
them. The file isn't stored. Our server log records only that an import
happened, with the install identifier, the file size and how many prices were
matched.

### 4. Quote calculations

To price a quote, the app sends the slab measurements and your rates (zones,
waste percentage, material and labour prices, extras) to our server's
calculation engine. **No client or business details are sent.** This step
doesn't use AI, and nothing is stored.

### 5. Install identifier and access tokens

The first time the app contacts our server, it creates a **random install
identifier**. The identifier isn't linked to your name, email, phone number or
device hardware, and we don't combine it with any other data. The app swaps it
for a 24-hour access token. We use the identifier only to:

- enforce fair-use limits (scans per month and requests per hour),
- protect the service from abuse and runaway costs, and
- link a crash or error report to a single install when we are
  troubleshooting.

Usage counters are kept only in the server's memory and reset whenever the
server restarts. Deleting the app deletes the identifier.

### 6. Crash reports

If the app crashes, it saves a short report on your device and sends a copy
to our server. The report contains the error message, the technical stack
trace, your platform (iOS or Android), the time, and the install identifier.
It does not include your quotes, client details or plans. Crash reports go
into our server logs so we can fix bugs.

### 7. Technical data

Like any internet service, our server and its hosting provider see technical
information about each request, such as your IP address and the time of the
request. We use your IP address, in memory only, for rate limiting and abuse
protection. Our hosting provider may keep standard request logs under its own
policies.

### 8. Subscriptions and payments

SlabIQ has a free tier and paid subscriptions. Purchases are processed by
**Apple (App Store)** or **Google (Play Store)**, and we never receive your
payment card details. Subscription status is managed by **RevenueCat**, which
receives an anonymous app user ID, your purchase and subscription history, and
basic device and app information such as platform and app version. Our server
may check your subscription status with RevenueCat to decide which usage
limits apply to you.

### 9. Camera and photos

SlabIQ asks for camera and photo library access **only** so you can
photograph a plan or pick a saved plan image to scan. It doesn't read your
photos in any other way. You can turn off these permissions at any time in
your device settings.

---

## Who we share information with

We share information only with the service providers SlabIQ needs in order to
work:

| Provider | What they receive | Why |
|---|---|---|
| **Anthropic** (Claude API) | Plans and rendered page images, job descriptions, price sheet contents | AI reading of plans and price sheets (kept up to 30 days, see below) |
| **Railway** | Everything sent to our server, while it is being processed | Hosting our processing server |
| **RevenueCat** | Anonymous app user ID, purchase history, device/app info | Managing subscriptions |
| **Apple / Google** | Purchase and payment details | Billing, under their own terms |

**About Anthropic.** Anthropic's
[Commercial Terms](https://www.anthropic.com/legal/commercial-terms) state
that it "may not train models on Customer Content" sent through its API.
SlabIQ reads plans with Claude Fable 5, which Anthropic classes as a
"Covered Model". For these models, Anthropic keeps prompts and outputs for
**30 days** to detect misuse, then deletes them. Our other AI steps (page
ranking and price-sheet checking) use models whose content Anthropic does not
keep by default. If Anthropic's automated safety systems flag a request, it
may keep that request for up to 2 years. Details:
[API and data retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention).

RevenueCat's policy is at [revenuecat.com/privacy](https://www.revenuecat.com/privacy).

We do not sell or rent personal information, and we don't share it for
advertising.

### Overseas processing

Our server and our providers may process information **outside Australia**,
mainly in the **United States**. We use established providers that have their
own security and privacy commitments. By using the plan reader or price-sheet
import, you understand that the files you choose will be processed overseas.

---

## Security

All communication between the app and our server is encrypted with HTTPS. Our
AI features need an access token that is issued to each install, and they are
protected by rate limits, usage quotas and a daily spending cap. Plan files
are held only as long as processing needs them.

Data on your device is protected by your device's own security, such as your
passcode and encryption. No system is perfectly secure. If you're not
comfortable with a document being processed by a third-party AI service,
please don't upload it.

---

## Your choices and rights

- **Your on-device data:** you can edit or delete estimates, clients and
  business details in the app. Uninstalling SlabIQ deletes all of its local
  data, including the install identifier.
- **Server-side data:** we don't keep an account or profile about you. Short
  technical logs, such as crash and error lines, are the only records linked
  to an install. If you want to ask what we hold, or ask us to delete
  something, email **slabiqapp@gmail.com**. If you can, include your install
  identifier.
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
