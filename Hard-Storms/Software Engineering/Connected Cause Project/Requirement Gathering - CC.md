#### Project Overview
1. What is the **Primary goal** of this project.?
	-  The primary goal of this project is to create a **charity donation platform** that acts as a **gateway between donors and charitable organizations**, with the unique model of enabling **micro-donations through round-up contributions**.
	- Whenever a user makes a purchase, the app rounds up the total to the nearest unit (e.g., $12.25 → $13.00) and collects the spare change ($0.75). These micro-donations accumulate over time and can be periodically donated (weekly/monthly) to selected charities or causes.
2. What is the **Secondary goal** of this project.?
	- Trust & Transparency
	- User control & Flexibility
	- Gamification & Engagement
	- Integration with Payment Systems
	- Scalability & Multi-Charity Support
	- Regulatory & Compliance Features
	- NGO / Charity Side Features
	- Admin Features
	- Accessibility & User Experience
	- Future Expansion Opportunities 
3. Who are the **end-users** of this system.?
	- Donor / Individual User[End-User]
	- Charity / NGO[End-User] 
	- System Admin[Supporting-User]
	- Corporate Partner[Optional, Future]
4. Are there **different types of users** or roles.?
	- **Donor** : Provide donations, Register/Login to platform, View Campaigns, Make donations, Track donation history, Receive receipts
	- **NGO/Charity Organization** : Receive and Manage Donations, Register their organizations, Create and manage campaigns, Update status on how funds are used, Upload proof of usage, Manage received donations
		- **System Admin** : Oversee and maintain the platform, Approve/reject NGO registrations, Monitor suspicious activities, Manage disputes between donors and NGOs, Maintain platform security and uptime.
5. Are there any **existing systems** the project needs to integrate with or replace.?
	- No existing systems need to be integrated or replaced at this stage, since this is a standalone POC built from scratch

#### Functional Requirements
1. What **core features** must the system have.?
	- User Management
	- NGO/Charity Management
	- Donation Mechanism
	- Wallet/Donation Pool
	- Charity Selection & Allocation
	- Receipts & Transparency
	- Notification & Reminder
	- Security & Compliance
	- Multi-currency & Global Support 
2. Are there any **secondary/optional features** desired for future versions.?
	- Transparency & Trust [Blockchain Based Donation Ledger & Smart Contracts]
	- Personalization & AI [AI driven Charity Recommendations, Donation Impact Prediction, Fraud Detection AI]
	- Engagement & Gamification [Leaderboards & Social Sharing, Donation Challenges]
	- Analytics & Reporting [Donor Dashboard, NGO Dashboard]
	- Voice Chatbot Donations
3. Are there any **specific workflows** the system must follow.?
	- Donor Onboarding Workflow
	- NGO Onboarding & Verification Workflow
	- Round-up Donation Workflow
	- Manual Donation Workflow
	- Donation Receipt & Transparency Workflow
	- Admin Workflow
	- Fraud Detection Workflow
	- Impact & Engagement Workflow
4. Should the system handle **multi-user collaboration** or real-time updates.?
	- Donation Confirmation
	- Wallet Updates
	- NGO Dashboard - Live Donation feed
	- Admin Fraud/Compliance Alerts
	- Impact Story / NGO Updates [Future]
5. Are there **notifications or alerts** needed.? (Email, SMS, in-app)
	- So yes — your system **definitely needs notifications & alerts**, but smartly categorized to avoid spamming users.
6. Are there any **reporting or analytics requirements**?
	- Yeah sure we would need, mainly Essential Dashboards for Donors, NGOs and Admin
7. Are there **user-generated content features**? (uploads, posts, comments)
	- For now -> No Requirement, might add in future as light community features.
8. Are there any **search, filter, or sorting capabilities** needed?
	- **Donor**
		- **Search** charities/NGOs by name.
		- **Filter** charities by : Category, Location & Type
		- **Sort** charities by : Impact Score, Most donation received & Newly added NGOs
	- **NGOs**
		- **Search** their own donor list (by donor name/email)
		- **Filter** donations by : Date Range, Amount & Status
		- **Sort** donations by : Highest Donation & Recent Donation
	- **Admin**
		- **Search** users (donors & NGOs)
		- **Filter** NGOs by verification status
		- **Sort** based on activity or donation volume
9. Are there **integration requirements**? (e.g., payment gateways, third-party APIs)
	- Payment Gateways -> this must handle Micro-transactions, Recurring collection, Refunds/disputes, PCI-DSS compliance -> e.g. Stripe, PayPal
	- Banking / Transaction APIs
	- Charity Verification APIs
	- Notification & Communication APIs
	- Identity Verification (KYC) APIs
	- Analytics & Tracking 
	- Optional Future Integrations like Blockchain, AI/ML, etc.
#### Non-Functional Requirements
1. What are the **performance expectations**? (e.g., response time, concurrent users)
	- This question ensures that the app won’t just “work,” but will **work fast, reliably, and at scale**, which is key for production.
	- Response Time Expectations
	- Concurrent Users
	- Transactions Per Second
	- System Availability
	- Data Consistency
	- Scalability Strategy
2. Are there **security requirements**? (e.g., encryption, GDPR, authentication/authorization methods)
	- Security requirements here are not optional — they are **foundational for trust + compliance** in any financial/charity app.
	- **Authentication & Authorization**
		- **JWT-based authentication** for users.
		- **OAuth 2.0 / OpenID Connect** (allow Google/Apple login).
		- **Role-based access control (RBAC)** → Donor, NGO, Admin.
		- **Multi-Factor Authentication (MFA)** for NGOs and Admins
	- **Encryption**
		- **Data-in-transit** → Enforce HTTPS/TLS 1.2+.
		- **Data-at-rest** → Encrypt sensitive fields (AES-256 for donor info, payment tokens).
		- **Password storage** → Hash + salt with algorithms like bcrypt/Argon2.
	- **Payment & Financial Security**
		- Must comply with **PCI-DSS** standards.
		- Never store raw credit card data → rely on **payment gateways** (Stripe, PayPal, etc.).
		- Support **tokenization** for recurring payments/round-ups.
	- **Data Privacy & Compliance**
		- **GDPR / CCPA compliance** → right to delete, export, or update personal data.
		- Explicit **user consent** for data usage (checkboxes during signup).
		- **Audit trails** for donations (who donated what, when).
	- **Fraud Prevention**
		- Detect suspicious transactions (e.g., multiple high donations from same IP).
		- **KYC checks** for NGOs to avoid fake charities.
		- Integrate **fraud detection APIs** (Stripe Radar, Sift).
	- **App & API Security**
		- Secure APIs with **rate limiting** (prevent DDoS/brute-force).
		- **Input validation** → prevent SQL injection/XSS.
		- **CORS policies** → whitelist domains.
		- **Regular penetration testing**.
	- **Monitoring & Alerts**
		- Real-time alerts for : 
			- Failed logins (possible brute force).
			- Suspicious donations.
			- System errors.
		- Integrate with **SIEM tools** (Splunk, ELK Stack).
3. Are there **availability or uptime requirements**?
	- So in your charity round-up app, we'd define **uptime requirements per phase**:
		- - POC → 99.5%
		- Production → 99.9%
		- Enterprise → 99.99%
4. Are there **scalability requirements**? (e.g., future growth in users or data)
	- User Scalability
	- Transaction Scalability
	- Data Scalability
	- Infrastructure Scalability
	- Geographic Scalability
	- Feature Scalability
5. Are there **platform requirements**? (Web, mobile, cross-platform, desktop)
	- For **POC** --> Donor Mobile App (cross platform) && NGO/Admin Web Dashboard
	- For **Production** --> Full mobile (iOS + Android) with App Store Deployment && Web Portals for NGOs and Admins
6. Are there **UI/UX expectations**? (Design style, themes, accessibility, responsiveness)
	- Minimal, Clean mobile UI for Donors.
	- Simple, functional web dashboard for NGOs/Admins.
	- Responsive layouts.
	- Add accessibility, dark mode, branding consistency.
	- More polished UX for reports, analytics, donation flows.

#### Data & Database
1. What **data needs to be stored** in the system? (User info, transactions, files, media, etc.)
	- User Data[Donors]
	- Charity / NGO Data
	- Transactions / Donations
	- Round-up Tracker
	- Reports & Analytics Data
	- Security & Auth Data
	- Notifications & Communication
	- Preferred Cause Categories[Optional]
	- Badges, Achievements, Donor Levels[Optional]
	- Media Uploads[Optional]
	- Donor Behavior, Personalized Recommendations[Optional]
	- Blockchain Ledger[Optional]
2. Are there **relationships between data**? (one-to-many, many-to-many, hierarchy)
	- User <--> Transaction [One-to-Many (1:N)]
	- User <--> Round-up Balances [One-to-Many (1:N)]
	- NGO <--> Transactions [One-to-Many (1:N)]
	- User <--> Payment Methods [One-to-Many (1:N)]
	- Notifications <--> Users / NGOS [One-to-Many (1:N)]
	- Admin <--> Audit Logs [One-to-Many (1:N)]
	- Users <--> NGOs [Many-to-Many (N:M)]
	- NGO <--> Cause Categories [Many-to-Many (N:M)]
3. Are there **file upload or media requirements**? (size limits, format restrictions)
	- Core file uploads --> NGO verification docs
	- Optional --> NGO media, user profile pictures, transaction receipts
	- Must enforce **size limits, format restrictions and access control**
4. Are there any **data retention or archival policies**?
	- **User Data**
		- **Retention Period:** Active while account exists + 2–5 years after account deletion (for audit/legal purposes).
		- **Archival:** Move deleted or inactive user data to a secure **cold storage** (encrypted).
		- **Compliance:** Must allow users to **request data deletion/export** per GDPR.
	- **Transaction / Donation Data**
		- **Retention Period:** Minimum 7 years (financial compliance, tax reporting).
		- **Archival:** Older transactions can be moved to a **read-only archival database** or cloud storage.
		- **Requirements:** Must remain **tamper-proof** for auditing. Consider blockchain-based ledger for immutable storage (optional).
	- **Round-Up Balances / Tracker**
		- **Retention Period:** Keep **historical cycles** at least 2–3 years for donor transparency.
		- **Archival:** Aggregate older cycles to save storage.
	- **NGO / Charity Documents**
		- **Verification Docs:** Keep indefinitely or until NGO deregisters.    
		- **Media Files:** Keep for **campaign relevance** (1–5 years) or until NGO removes them.
	- **Logs / Audit Trails**
		- **Retention Period:** 1–3 years (system logs, admin actions, security logs).
		- **Archival:** Compressed and moved to cold storage for historical auditing.
		- **Security:** Encrypted and access-controlled.
	- **Notification / Communication Logs**
		- **Retention Period:** 6–12 months
		- **Archival:** Aggregate older notifications for analytics if needed.
	- **Implementation Notes**
		- **Automation:** Scheduled jobs to archive old data. Soft-delete mechanism before permanent deletion.
		- **Regulatory Compliance:** Ensure data deletion respects local laws. Encrypt all archived data.
5. Remaining areas for future : DB Type, Indexing, Backup / Recovery, Analytics layer, Multi-tenancy, Advance Features
#### Authentication & Authorization
1. How will users **sign up or log in**? (Email/password, social login, OTP)
	- Core methods : **Email/password**[mandatory]
	- Optional methods : **Social Login** || **OTP Login**
2. Will there be **role-based access control**?
	- Yes, Admin && Donor && Charity Organization
3. Should there be **multi-factor authentication (MFA)**?
	- Yes, you should implement a MFA.
4. Any **sensitive data** that needs **special handling**?
	- User Authentication
	- MFA
	- Role Based Access Control
	- Sensitive Data Handling
	- Data Transmission & Storage
	- Session & Token Management
	- Logging & Monitoring
	- Optional Enhancements

#### UI / UX
1. Any **reference websites or apps** that the client likes?
	- `GoFundMe`
	- `Ketto`
	- `GlobalGiving`
	- `GiveIndia`
2. Should the design be **minimalistic, modern, dashboard-heavy, or something else**?
	- Minimalistic
	- Modern
	- Storytelling visuals, Trust cues, Emotional triggers & Positive reinforcement
	- Light Dashboard Elements 
3. Should it be **mobile-first/responsive**?
	- Yes, absolutely.
4. Are there **custom themes or branding guidelines** to follow?
	- We will discuss this and create one branding guideline.

#### Notifications & Communication
1. Are **emails, SMS, push notifications** required?
	- Yes, it should have all three : **Email, SMS & Push**.
2. What **events or actions** should trigger notifications?
	- **Donors** --> Confirmation, updates, impact.
	- **Charities** --> Donations, approvals, cause activity.
	- **Admins** --> Moderation, approvals, system security.
3. Should users be able to **customize notification preferences**?
	- Yes, allowing users to customize notification preferences is highly recommended. It improves user experience, reduces *notification fatigue*, and increase engagement.

#### Reporting & Analytics
1. Are there any **dashboard or reporting features**?
2. Should reports be **exportable**? (PDF, Excel, CSV)
3. Are **analytics on user behavior or system usage** required?

#### Deployment & Production
1. Any **hosting/cloud preferences**? (AWS, Azure, GCP, on-prem)
2. Are there **CI/CD or automated deployment requirements**?
3. Any **backup, monitoring, or logging requirements**?

#### Maintenance & Future Expansion
1. How often should the system be **updated or maintained**?
2. Are there plans to **add new features in the future**?
3. Any requirements for **modularity or plugin-based architecture**?

#### Budget & Timeline
1. Are there any **budget constraints**?
2. What is the **expected timeline** for MVP/POC?
3. Are there **phased deliverables** or just a single launch?

#### Brainstorming 
- Approaches that can be used to Donate: 
	- Round-up donation model[currently used]
	- Direct % Contribution (sets a percentage of each purchase, e.g. 1% of total, then if $100 spends -> $1 goes to charity)
	- Subscription style giving (fixed small amount per week or month)
	- Gamified Donation[something I would like to integrate with the existing approach]
	- Corporate Tie-ins (if the employer donates  $20 -> the company donates $20)
	- Charity "Bucket" (pick-up a cause, round-up goes into the bucket)
	- Event Based Micro-donations (when I order coffee -> donate $2)
- Challenges to Consider
	- Payments Integration
	- Trust & Transparency
	- Legal Compliance
	- User Adoption
- User Journey Diagrams (UX)
- System Requirements
- **Functional Requirements left** → notifications, search/discovery, reporting, refund/dispute, multilingual, multiple payment options.
- **Non-functional Requirements left** → performance, availability, maintainability, extensibility, compliance, logging, backup/recovery.