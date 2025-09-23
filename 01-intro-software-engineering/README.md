# 01 — Intro to Software Engineering

This module covers the foundations of **Software Engineering (SE)** and SDLC.  
As a hands-on exercise, I produced a **Mini Blog System — Documentation Project** to simulate a real workflow.

> ℹ️ TH: โมดูลนี้เน้น “กระบวนการและเอกสาร” มากกว่าโค้ด เพื่อเตรียมพร้อมก่อนสร้างระบบจริง

---

## 🎯 Learning Outcomes
- Understand **SDLC** phases: Requirements → Design → Implementation → Testing → Release → Maintenance.
- Produce **professional documentation** artifacts (URS, SRS, SysRS, Design/UML, Test Plan, Roles).
- Practice version control & portfolio presentation on GitHub.

---

## 📑 Documentation Index
- [URS – User Requirement Specification](mini-blog-docs/docs/URS.md)  
- [SRS – Software Requirement Specification](mini-blog-docs/docs/SRS.md)  
- [SysRS – System Requirement Specification](mini-blog-docs/docs/SysRS.md)  
- [System Design & UML](mini-blog-docs/docs/design.md)  
- [Test Plan](mini-blog-docs/docs/test-plan.md)  
- [Roles & Responsibilities](mini-blog-docs/docs/roles.md)

---

## 🏗️ High-Level Architecture
```mermaid
flowchart LR
  U[User] --> FE[Frontend: HTML/CSS/JS]
  FE --> BE[Backend: Node.js + Express]
  BE --> DB[(MongoDB Atlas)]
