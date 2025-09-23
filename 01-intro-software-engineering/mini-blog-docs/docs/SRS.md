# SRS — Software Requirement Specification

> ℹ️ TH: “ข้อกำหนดเชิงซอฟต์แวร์” ที่วัดผลได้ และทดสอบได้

---

## 1) Functional Requirements (FR)
**FR-001 — Authentication**  
- Users can register with email/password.  
- Users can log in/out and maintain a session.

**FR-002 — Post CRUD**  
- Create, Read (list/detail), Update (author only), Delete (author only).  
- Required fields: title, body, authorId, createdAt.

**FR-003 — Public Reading**  
- Anyone can list & view public posts without login.

**FR-004 — Search/Filter (basic)**  
- Filter by keyword in title (v1).

**FR-005 — Authorization**  
- Only the post owner can edit/delete their post.

---

## 2) Non-Functional Requirements (NFR)
**NFR-001 Performance** — p95 list page < 800ms @ 100 concurrent users.  
**NFR-002 Security** — Passwords hashed (e.g., bcrypt); OWASP ASVS basics.  
**NFR-003 Availability** — 99% monthly uptime (initial target).  
**NFR-004 Usability** — Mobile-responsive layout; accessible form labels.  
**NFR-005 Maintainability** — Code linting & basic CI check (later).  
**NFR-006 Observability** — Basic request logging and error tracking.

---

## 3) Data Requirements
- **Post**: id, title, body, authorId, createdAt, updatedAt, status (draft/published).  
- **User**: id, email, passwordHash, displayName, createdAt.

---

## 4) Interfaces & API (placeholder)
- REST over HTTPS (JSON).
- Auth: `/api/auth/register`, `/api/auth/login`, `/api/auth/logout`  
- Posts: `/api/posts` (GET/POST), `/api/posts/:id` (GET/PUT/DELETE)

> ℹ️ TH: รายละเอียดสัญญา API (request/response) จะระบุในเอกสาร Design

---

## 5) Error Handling & Validation
- Validation errors return 400 with field messages.
- Unauthorized returns 401; forbidden 403; not found 404.

---

## 6) Traceability
| URS Story | SRS FR/NFR | Test Case |
|---|---|---|
| US-002 | FR-001, NFR-002 | TC-AUTH-01..03 |
| US-003 | FR-002, FR-005 | TC-POST-01..06 |

---

## 7) Risks & Mitigations
- **Weak passwords** → enforce minimum complexity; hash with salt.  
- **Spam content** → rate limit post creation (future).
