# Privacy Policy

> **Last Updated:** October 17, 2026  
> **Effective Date:** October 17, 2026  
> **Version:** 2.0.0  
> **Data Controller:** QIMEM Technologies PLC ("QIMEM", "Company", "we", "us", or "our")  
> **Applicable Products:** MyDelala Mobile Applications (Android & iOS), MyDelala Web Portal, Telegram Mini App, and Backend APIs  
> **Official Website:** [https://mydelala.qimemtech.com](https://mydelala.qimemtech.com)  
> **Privacy Inquiries & DPO:** [privacy@qimemtech.com](mailto:privacy@qimemtech.com)

---

## Table of Contents

1. [Introduction & Scope](#1-introduction--scope)
2. [Information We Collect](#2-information-we-collect)
3. [Prominent Disclosure: Precise Location & Background Location Tracking](#3-prominent-disclosure-precise-location--background-location-tracking)
4. [Device Permissions & Hardware Access (Android & iOS)](#4-device-permissions--hardware-access-android--ios)
5. [Purposes & Legal Bases for Data Processing](#5-purposes--legal-bases-for-data-processing)
6. [Sharing, Disclosure & International Transfer of Information](#6-sharing-disclosure--international-transfer-of-information)
7. [Enterprise Security Architecture & Data Safeguards](#7-enterprise-security-architecture--data-safeguards)
8. [Account Deletion, Data Retention & Erasure (Google Play Compliance)](#8-account-deletion-data-retention--erasure-google-play-compliance)
9. [Your Legal Rights & Privacy Choices (GDPR, CCPA & Local Laws)](#9-your-legal-rights--privacy-choices-gdpr-ccpa--local-laws)
10. [Children's Privacy Protection (Under 18 Policy)](#10-childrens-privacy-protection-under-18-policy)
11. [Cookies, Telemetry & Analytical Technologies](#11-cookies-telemetry--analytical-technologies)
12. [Third-Party Services, SDKs & External Gateways](#12-third-party-services-sdks--external-gateways)
13. [Changes to this Privacy Policy](#13-changes-to-this-privacy-policy)
14. [Contact Information & Data Protection Officer](#14-contact-information--data-protection-officer)

---

## 1. Introduction & Scope

**QIMEM Technologies PLC** is committed to protecting your fundamental right to privacy, confidentiality, and data sovereignty. This Privacy Policy applies to all users ("you", "your", "Seeker", "Broker", "Agency", or "Owner") accessing the **MyDelala** ecosystem across our mobile applications on the Google Play Store and Apple App Store, our responsive web portals, Telegram Mini Apps, and cloud API endpoints.

This Privacy Policy explains transparently:

- What categories of personal, biometric, technical, and geolocation data we collect;
- Why and on what legal bases we process this data;
- How we protect your data through advanced architectural safeguards (including PostgreSQL Row-Level Security, Argon2id/Bcrypt hashing, and PII log scrubbing);
- Our strict adherence to global privacy frameworks (EU General Data Protection Regulation - **GDPR**, California Consumer Privacy Act - **CCPA**, and Ethiopian Personal Data Protection and Electronic Commerce Directives);
- Our compliance with the **Google Play Developer Program Policies**, particularly regarding User Data, Location In The Background, Device Permissions, and Account Deletion.

---

## 2. Information We Collect

We collect information directly from you, automatically through your device interactions, and from verified government authentication partners.

### 2.1 Information You Provide to Us

| Category | Specific Data Elements | Purpose & Usage |
| :--- | :--- | :--- |
| **Account Identity** | Full name, mobile telephone number, email address, profile picture / avatar, user bio, specialization tags, and preferred language. | User account creation, profile display, role assignment, and multi-factor authentication. |
| **Authentication Credentials** | Cryptographic password hashes, One-Time Password (OTP) verification tokens, and social identity linkages (Telegram, Google, Apple). | Securing your account access, session token generation, and credential management. |
| **KYC & Identity Verification** | Ethiopian National ID (**Fayda**) verification tokens, National ID Card / Passport images, Taxpayer Identification Numbers (TIN), Real Estate Brokerage licenses, Commercial Registration documents, and live verification selfie images. | Mandatory fraud prevention, legal compliance, and provider verification before marketing properties to consumers. |
| **Property Listings & Media** | Property photographs, video walkthroughs, floor plans, geographic addresses, price structures, lease terms, title deeds, and property amenity details. | Indexing, publishing, and displaying real estate listings to interested seekers on the platform. |
| **In-App Communications** | Direct chat messages, audio/image attachments, appointment negotiation notes, dispute reports, and customer service inquiries. | Facilitating deal negotiations between parties, customer dispute resolution, and community safety enforcement. |
| **Safety, Blocking & Abuse Reports** | Blocked counterparty identifiers, abuse reports, violation category, narrative description of abusive behavior, screenshots or attached evidence, and administrative resolution records. | Enforcing interpersonal blocking safeguards, investigating abuse, complying with Google Play Store safety directives, and maintaining community standards. |
| **Reputation & Feedback** | Numerical ratings, textual reviews, provider public responses, and platform satisfaction surveys. | Fostering trust, accountability, and marketplace quality control. |

### 2.2 Information Collected Automatically Through Your Use

| Category | Specific Data Elements | Purpose & Usage |
| :--- | :--- | :--- |
| **Precise Geolocation** | Latitude, longitude, GPS altitude, movement speed, horizontal accuracy, and timestamped telemetry. | Finding nearby properties, verified broker proximity discovery, transit tracking during property viewings, and anti-spoofing fraud defense. |
| **Device & Network Data** | Device brand, model, operating system version, unique device identifier (UUID), IP address, mobile carrier, browser user-agent, and client API keys (`X-Platform-Client`). | Security defense, session device management, bot mitigation (`BlockBadBots`), and client platform access control. |
| **Push Notification Tokens** | Firebase Cloud Messaging (FCM) registration tokens and active device session tokens. | Delivering real-time push alerts for appointment updates, incoming chat messages, and account security notifications. |
| **LiveKit WebRTC Signaling** | Temporary WebRTC session connection metadata, participant socket room tokens, and call duration logs. | Powering end-to-end peer-to-peer audio and video calling between seekers and brokers. |
| **Transaction & Billing Logs** | Payment gateway reference identifiers (Telebirr, Chapa, CBE Birr), invoice numbers, subscription packages, quota allocations, and bank deposit slip images. | Processing service purchases, issuing tax-compliant VAT invoices, quota tracking, and accounting compliance. |

> **IMPORTANT NOTICE REGARDING FINANCIAL DATA:**  
> QIMEM Technologies PLC does **NOT** collect, process, or store raw credit/debit card numbers, CVVs, or mobile banking PINs. All monetary transactions are processed directly by certified, licensed, PCI-DSS compliant payment gateways (**Ethio Telecom Telebirr**, **Chapa Financial Technologies**, and **Commercial Bank of Ethiopia CBE Birr**).

---

## 3. Prominent Disclosure: Precise Location & Background Location Tracking

> [!IMPORTANT]  
> **GOOGLE PLAY DEVELOPER POLICY DISCLOSURE — LOCATION DATA**  
> MyDelala collects and processes both **Foreground** and **Background** location data to enable essential real-time real-estate matching, appointment transit tracking, and GPS fraud prevention.

### 3.1 Why MyDelala Collects Location Data

Real estate brokerage requires physical presence and geographical proximity. MyDelala uses precise location data for:

1. **Nearby Property & Broker Discovery (Foreground):** When you use the app, we utilize your current GPS coordinates to display properties, apartments, and verified brokers located within your immediate radius.
2. **Scheduled Viewing Transit Tracking (Background — Providers Only):** For verified Brokers and Agencies on active duty who have a confirmed in-person property viewing appointment with a Seeker, the app collects location data **in the background (even when the app is closed or not in active screen focus)** to:
   - Provide the waiting Seeker with a real-time transit estimate (ETA) and arrival confirmation.
   - Ensure the physical safety of both parties during unfamiliar property inspections.
   - Verify that the provider is genuinely traveling toward and present at the physical property location.
3. **GPS Anti-Spoofing & Marketplace Integrity:** Our automated security subsystem (`GpsSpoofBlocker`) evaluates hardware telemetry to detect and prevent mock location apps, GPS spoofing utilities, and synthetic location manipulation.

### 3.2 User Control & Transparency

- **Opt-In Consent:** Background location is never initiated without your explicit, separate runtime permission prompt.
- **Provider Duty Toggle:** Verified providers can toggle their active duty / visibility status **OFF** at any time within their app dashboard (`my/working-hours` and `providers/visibility`), which immediately halts background telemetry transmission.
- **Never Sold or Monetized:** We **NEVER** sell, rent, license, or disclose your personal location telemetry to advertisers, data brokers, or commercial marketing syndicates.

---

## 4. Device Permissions & Hardware Access (Android & iOS)

To deliver our services, the MyDelala mobile applications request access to specific hardware and system capabilities. Below is a complete breakdown of every sensitive permission requested, its technical identifier, and its strict justification:

| Permission Name (Android / iOS) | Required / Optional | Technical Justification & Use Case |
| :--- | :---: | :--- |
| `ACCESS_FINE_LOCATION`<br>`ACCESS_COARSE_LOCATION` | Required for Map Features | Calculates distance to listings, places the user accurately on interactive maps, and discovers nearby verified real estate providers. |
| `ACCESS_BACKGROUND_LOCATION` | Optional (Providers Only) | Enables active brokers and agencies to transmit heartbeat location telemetry during transit to scheduled property viewing appointments, even when the screen is locked or another app is open. |
| `CAMERA` | Optional | Allows users to capture property photographs, video tours, upload profile pictures, capture verification selfies, scan national ID documents for KYC, and participate in LiveKit WebRTC video calls. |
| `READ_MEDIA_IMAGES`<br>`READ_EXTERNAL_STORAGE` | Optional | Enables users to select and upload existing property photos, architectural blueprints, PDF ownership deeds, and bank deposit receipts from the device gallery. |
| `RECORD_AUDIO` | Optional | Required strictly when initiating or answering live peer-to-peer voice and video calls with brokers or clients via LiveKit WebRTC. |
| `POST_NOTIFICATIONS` | Optional (Recommended) | Transmits critical Firebase Cloud Messaging (FCM) alerts for appointment confirmations, reschedule requests, chat messages, and security notices. |

You may revoke any of these permissions at any time via your device's operating system settings (`Settings → Apps → MyDelala → Permissions`). Revoking certain permissions (such as Location or Camera) may limit your ability to use specific features (such as map exploration or video calling).

---

## 5. Purposes & Legal Bases for Data Processing

In accordance with international standards (GDPR Art. 6) and Ethiopian legal frameworks, we process your personal data under the following lawful bases:

| Processing Purpose | Categories of Data | Legal Basis (GDPR / Statutory) |
| :--- | :--- | :--- |
| **Service Provision & Contract Execution** | Account details, listings, bookings, messaging, call connection data, payments. | **Contractual Necessity:** Processing is required to perform the Terms and Conditions entered into with you. |
| **Identity Verification & Anti-Fraud** | Fayda National ID tokens, government IDs, broker licenses, selfies, GPS spoof screening. | **Legal Obligation & Legitimate Interest:** Preventing fraud, money laundering, and illegal real estate brokerage practices. |
| **Background Transit Tracking** | Background GPS coordinates of verified providers during scheduled appointments. | **Explicit Consent & Legitimate Interest:** Ensuring consumer safety, transit predictability, and appointment verification. |
| **Invoicing & Tax Compliance** | Legal name, TIN, purchase histories, VAT invoices, payment audit trails. | **Legal Obligation:** Complying with Ethiopian Revenue and Customs Authority (ERCA) financial record-keeping laws. |
| **Platform Cybersecurity & Threat Defense** | IP addresses, request headers, error logs, audit logs, device fingerprints. | **Legitimate Interest:** Protecting infrastructure against DoS attacks, bot exploitation, SSRF, and data breaches. |

---

## 6. Sharing, Disclosure & International Transfer of Information

We treat your personal information with strict confidentiality. We share data only under defined circumstances:

### 6.1 Marketplace Counterparties

To facilitate property discovery and viewings:

- **Public Profile:** A Provider's business name, profile photo, verified badge, average review rating, and public listings are accessible to all users.
- **Confirmed Appointments:** Once an appointment is confirmed, the Seeker's contact information and the Provider's direct telephone number and appointment location are shared between the two parties.

### 6.2 Trusted Third-Party Infrastructure Providers

We engage specialized, enterprise-grade technology processors bound by strict Data Processing Agreements (DPAs):

- **Payment Gateways:** Ethio Telecom (Telebirr), Chapa Financial Technologies, Commercial Bank of Ethiopia (CBE Birr).
- **Cloud Infrastructure & Managed Databases:** Encrypted cloud hosting and Neon / PostgreSQL enterprise database clusters with automated backups.
- **Communications & WebRTC:** Google Firebase Cloud Messaging (FCM for push notifications) and LiveKit Inc. (WebRTC video and audio infrastructure).
- **Identity & National Registry:** National ID Program of Ethiopia (Fayda / eSignet) for identity verification.

### 6.3 Legal Compliance & Protection of Rights

We may disclose personal data to law enforcement, judicial bodies, the Ethiopian Information Network Security Administration (**INSA**), or regulatory authorities if:

- Required by a valid court order, search warrant, or statutory subpoena.
- Necessary to investigate suspected fraud, phantom listings, property extortion, or criminal conduct.
- Necessary to protect the physical safety, property, or legal rights of our users, employees, or the public.

---

## 7. Enterprise Security Architecture & Data Safeguards

As detailed in our [Company Security Standards](docs/SECURITY_STANDARDS.md), QIMEM implements defense-in-depth safeguards across every tier:

```
┌────────────────────────────────────────────────────────┐
│ Transport Layer: TLS 1.3 / HTTPS Encryption Everywhere │
├────────────────────────────────────────────────────────┤
│ Perimeter: Rate-Limiting, Bot-Blocking & SSRF Guard   │
├────────────────────────────────────────────────────────┤
│ Application: Strict Granular RBAC (checkPermission)    │
├────────────────────────────────────────────────────────┤
│ Database: PostgreSQL Row-Level Security (RLS) Isolation │
├────────────────────────────────────────────────────────┤
│ Data at Rest: AES-256 Storage & Argon2id Password Hash │
└────────────────────────────────────────────────────────┘
```

1. **PostgreSQL Row-Level Security (RLS):** Database queries are isolated at the database engine kernel level using tenant and user session injection (`app.current_user_id`), rendering Insecure Direct Object References (IDOR) impossible.
2. **Password Security:** Passwords are never stored in plain text. We utilize salted, high-entropy hashing algorithms (Argon2id and Bcrypt with a minimum cost factor of 12) with anti-recycling history tracking.
3. **Sensitive PII Scrubbing:** Application logs, error monitoring tools (Sentry), and audit trails employ automated scrubbers (`SensitiveDataScrubber`) that systematically redact national IDs, telephone numbers, passwords, and authorization tokens.
4. **Secure Media Isolation:** Uploaded KYC identity documents and business licenses are stored in private, unguessable UUID-based storage disks accessible only by authorized compliance personnel via time-limited signed URLs.

---

## 8. Account Deletion, Data Retention & Erasure (Google Play Compliance)

> [!IMPORTANT]  
> **GOOGLE PLAY ACCOUNT DELETION COMPLIANCE**  
> You have the absolute right to permanently delete your MyDelala account and all associated personal data at any time, both from within the mobile application and via our external web portal.

### 8.1 How to Delete Your Account

We provide three simple, accessible deletion pathways:

1. **In-App Deletion (Mobile):**  
   Open the MyDelala app → Navigate to `Profile` → `Settings` → `Privacy & Security` → Select **"Delete Account"** → Enter your password/OTP to confirm.
2. **Dedicated Web Deletion Portal (No app required):**  
   Visit our public account deletion portal at:  
   👉 **[https://mydelala.qimemtech.com/delete-account](https://mydelala.qimemtech.com/delete-account)**
3. **Direct Email Request:**  
   Send an email with the subject line *"Account Deletion Request"* from your registered email address to **[privacy@qimemtech.com](mailto:privacy@qimemtech.com)**.

### 8.2 The 30-Day Grace Period & Permanent Erasure Process

To protect users against accidental deletion or unauthorized account hijack:

- **Phase 1: Immediate Deactivation (Days 1–30):** Your profile, public listings, active appointments, and broker badges are immediately hidden from all marketplace search results and public views. If you log back into your account within thirty (30) calendar days, you may cancel the deletion request and restore your account.
- **Phase 2: Irreversible Scrubbing (Day 31+):** Once the 30-day grace period concludes, our automated purging system permanently anonymizes your record:
  - Phone number is scrubbed and permanently overwritten with an anonymized sentinel value (`+999000000000`).
  - Name is replaced with `[Deleted User]`.
  - Profile pictures, KYC documents, broker licenses, and device tokens are permanently destroyed from our storage disks.
  - Social login links (Telegram, Google, Apple) are unlinked and session caches are flushed.

### 8.3 Data Retained for Statutory Legal & Tax Obligations

Under Ethiopian commercial, taxation, and anti-money laundering legislation:

- Completed financial invoices, VAT receipts, and transaction records must be retained for the minimum statutory retention period (ten (10) years) required by the Ethiopian Revenue and Customs Authority (ERCA).
- Historical audit logs recording administrative moderation actions or financial transfers are archived in anonymized form for regulatory compliance and dispute defense.

### 8.4 Blocked Users Data & Abuse Report Evidence Retention

In accordance with mobile platform compliance and user protection standards:

- **Blocked Users Registry:** When you block another user, the blocking record (`user_id`, `blocked_user_id`, reason, and timestamp) is stored to enforce real-time communication filtering across chat, calls, appointments, and service requests. If you delete your account, your active block records are anonymized and released.
- **Abuse Reports & Moderation Evidence:** In order to comply with international consumer safety laws and mobile app store mandates, records of submitted abuse reports (`reporter_id`, `reported_user_id`, category, evidence descriptions, resolution notes) are retained for a period of up to three (3) years to prevent serial bad actors, fraud syndicates, and repeated harassment. When an account is deleted, the user's personal identity is scrubbed, while the incident report history remains preserved for safety analytics and legal compliance.

---

## 9. Your Legal Rights & Privacy Choices (GDPR, CCPA & Local Laws)

Depending on your geographic residency, you possess extensive statutory privacy rights:

| Right | What It Means for You | How to Exercise |
| :--- | :--- | :--- |
| **Right of Access / Portability** | Request a machine-readable copy (JSON/CSV) of all personal data we maintain about you. | Email [privacy@qimemtech.com](mailto:privacy@qimemtech.com) or download via the Web Portal. |
| **Right to Rectification** | Correct inaccurate, out-of-date, or incomplete profile or property information. | Update directly via `Profile → Edit Profile` or contact support. |
| **Right to Erasure ("Right to be Forgotten")** | Demand the permanent deletion of your account and personal data. | Follow the steps outlined in Section 8. |
| **Right to Restrict Processing** | Restrict how we process your data while an investigation or dispute is pending. | Submit a formal restriction notice to our DPO. |
| **Right to Withdraw Consent** | Revoke consent previously granted for location tracking, push notifications, or camera access. | Adjust operating system permissions on your mobile device at any time. |
| **CCPA "Do Not Sell" Disclosure** | We **do not sell or share** your personal data with third-party data brokers for commercial monetization. | Applicable to all users globally by default. |

To exercise any of these rights, contact our Data Protection Officer at **[privacy@qimemtech.com](mailto:privacy@qimemtech.com)**. We respond to and fulfill verified privacy requests within **thirty (30) business days** without charge.

---

## 10. Children's Privacy Protection (Under 18 Policy)

MyDelala is strictly designed, intended, and operated for individuals who are **eighteen (18) years of age or older**. Real estate discovery, property leasing, commercial transactions, and broker engagements involve legally binding contracts that minors cannot execute under Ethiopian law.

We do not knowingly solicit, collect, or process personal data from children under the age of 18. If we become aware that an account has been registered by a minor under 18, we will immediately freeze the account, cancel pending appointments, and permanently purge all associated personal information from our databases. If you believe a minor has provided us with personal information, please notify us immediately at [privacy@qimemtech.com](mailto:privacy@qimemtech.com).

---

## 11. Cookies, Telemetry & Analytical Technologies

### 11.1 Web Portal Cookies

When using our web applications ([https://mydelala.qimemtech.com](https://mydelala.qimemtech.com) and [https://delala-admin.qimemtech.com](https://delala-admin.qimemtech.com)), we employ essential session cookies and security tokens:

- **Authentication Cookies:** Secure, HTTP-only, SameSite cookies maintaining your active dashboard session.
- **CSRF Tokens:** Cross-Site Request Forgery tokens preventing malicious sites from executing unauthorized actions on your behalf.
- **Locale & Preference Cookies:** Storing your chosen interface language (English, Amharic, Oromo, Tigrinya).

We do **NOT** deploy third-party advertising cookies, cross-site trackers, or behavioral advertising tracking pixels.

---

## 12. Third-Party Services, SDKs & External Gateways

Our mobile and web applications incorporate trusted third-party Software Development Kits (SDKs) essential for platform functionality:

| Third-Party Partner / SDK | Service Provided | Privacy Policy Reference |
| :--- | :--- | :--- |
| **Google Play Services / FCM** | Push notifications, device integrity, app distribution. | [Google Privacy Policy](https://policies.google.com/privacy) |
| **Ethio Telecom (Telebirr)** | Mobile payment processing & gateway checkout. | [Ethio Telecom Privacy Terms](https://www.ethiotelecom.et) |
| **Chapa Financial Technologies** | Card, bank, and digital payment gateway services. | [Chapa Privacy Policy](https://chapa.co/privacy-policy) |
| **LiveKit Inc.** | Open-source WebRTC media server for audio/video calling. | [LiveKit Privacy Policy](https://livekit.io/privacy) |
| **Sentry (Functional Software)** | Automated error monitoring & crash diagnostics (PII scrubbed). | [Sentry Privacy Policy](https://sentry.io/privacy) |

---

## 13. Changes to this Privacy Policy

We may update this Privacy Policy periodically to reflect enhancements in our application features, technological advancements, or changes in statutory data protection laws.

- When material modifications occur, we will update the **"Last Updated"** date at the top of this document and publish a prominent notification banner within the mobile application or send an email alert to registered users.
- Your continued use of the Platform after the effective date of an updated Privacy Policy constitutes your informed acknowledgment and acceptance of the revised practices.

---

## 14. Contact Information & Data Protection Officer

If you have questions, concerns, complaints, or requests regarding this Privacy Policy, your personal data, or our privacy practices, please contact our Data Protection Team:

**QIMEM Technologies PLC**  
Attn: Data Protection Officer (DPO) / Privacy Team  
Bole Sub-City, Addis Ababa, Ethiopia  

- **Official Privacy Email:** [privacy@qimemtech.com](mailto:privacy@qimemtech.com)  
- **General Inquiries:** [info@qimemtech.com](mailto:info@qimemtech.com)  
- **Customer Support:** [support@qimemtech.com](mailto:support@qimemtech.com)  
- **Account Deletion Portal:** [https://mydelala.qimemtech.com/delete-account](https://mydelala.qimemtech.com/delete-account)  
- **Telegram Official Bot:** [@my_delalabot](https://t.me/my_delalabot)
