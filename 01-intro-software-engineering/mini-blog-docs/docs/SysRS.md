# SysRS — System Requirement Specification

> ℹ️ TH: ข้อกำหนดระดับ “ระบบ” เช่น สถาปัตยกรรม สภาพแวดล้อม ข้อจำกัด

---

## 1) Architecture Overview
- Web client (HTML/CSS/JS) ↔ REST API (Node.js/Express) ↔ MongoDB Atlas.
- Stateless API; JWT/session cookie (v1: simple session ok).

```mermaid
flowchart LR
  Client[Web Client] --> API[Node.js / Express API]
  API --> DB[(MongoDB Atlas)]
