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
	- 
8. Are there any **search, filter, or sorting capabilities** needed?
9. Are there **integration requirements**? (e.g., payment gateways, third-party APIs)

#### Non-Functional Requirements
1. What are the **performance expectations**? (e.g., response time, concurrent users)
2. Are there **security requirements**? (e.g., encryption, GDPR, authentication/authorization methods)
3. Are there **availability or uptime requirements**?
4. Are there **scalability requirements**? (e.g., future growth in users or data)
5. Are there **platform requirements**? (Web, mobile, cross-platform, desktop)
6. Are there **UI/UX expectations**? (Design style, themes, accessibility, responsiveness)

#### Data & Database
1. What **data needs to be stored** in the system? (User info, transactions, files, media, etc.)
2. Are there **relationships between data**? (one-to-many, many-to-many, hierarchy)
3. Are there **file upload or media requirements**? (size limits, format restrictions)
4. Are there any **data retention or archival policies**?

#### Authentication & Authorization
1. How will users **sign up or log in**? (Email/password, social login, OTP)
2. Will there be **role-based access control**?
3. Should there be **multi-factor authentication (MFA)**?
4. Any **sensitive data** that needs **special handling**?

#### UI / UX
1. Any **reference websites or apps** that the client likes?
2. Should the design be **minimalistic, modern, dashboard-heavy, or something else**?
3. Should it be **mobile-first/responsive**?
4. Are there **custom themes or branding guidelines** to follow?

#### Notifications & Communication
1. Are **emails, SMS, push notifications** required?
2. What **events or actions** should trigger notifications?
3. Should users be able to **customize notification preferences**?

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