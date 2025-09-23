# URS — User Requirement Specification

> ℹ️ TH: ระบุ “ใครใช้ระบบ” และ “ผู้ใช้ต้องการอะไร” โดยไม่ผูกกับเทคโนโลยี

---

## 👥 Personas & Roles
- **Visitor** — reads public posts only.
- **Registered User (Author)** — signs up / signs in, creates/edits/deletes *own* posts.
- **Admin (optional)** — moderates content & manages users.

---

## 🎯 Top-Level User Goals
1. Discover and read public posts easily.
2. Author posts with minimal friction.
3. Manage own content safely (edit/delete).
4. Trust the platform (basic security, uptime).

---

## 🧩 User Stories (MoSCoW)
> Format: *As a [role], I want [capability], so that [benefit].*

### Must-Have
- **US-001** — As a Visitor, I want to browse posts, so that I can read content.  
- **US-002** — As a User, I want to register & log in, so that I can publish posts.  
- **US-003** — As a User, I want to create/edit/delete my posts, so that I can manage my content.

### Should-Have
- **US-004** — As a Visitor/User, I want search/filter, so that I can find posts quickly.

### Could-Have
- **US-005** — As a User, I want to draft posts, so that I can publish later.

### Won’t-Have (v1)
- **US-006** — Social sharing & comments.

---

## ✅ Acceptance Criteria (samples)
- **US-002** (Register/Login)  
  - **Given** a new user, **when** they submit valid info, **then** the account is created and user is authenticated.
  - **Given** an existing user, **when** they provide correct credentials, **then** they access their dashboard.

- **US-003** (CRUD Posts)  
  - **Given** I’m logged in, **when** I create a post with required fields, **then** it appears in my feed.
  - **Given** I’m the author, **when** I edit/delete my post, **then** changes reflect immediately and are persisted.

---

## 🔒 Constraints & Assumptions
- Basic email/password auth (no SSO in v1).
- Public content readable without login.
- Desktop + mobile web (responsive) in v1.

---

## 📌 Success Metrics
- TTFP (time to first post) < 5 minutes after signup.
- 95% tasks success rate on basic flows (browse, register, create).

---

## ❓ Open Questions
- Should posts support images/video in v1?
- Any localization requirements?
