# Day 2: OWASP Top 10

**What I learned:**
- The OWASP Top 10 is the top 10 most critical web application security risks ranked by how common and how damaging they are.
- Web security comes down to 4 questions:
  1. Who are you ? (identity)
  2. What are you allowed to do ? (permissions)
  3. Can I trust what you send me ? (input)
  4. Did I build and run this safely ? (the whole system)
- IDOR is when when you can reach another user’s data just by changing an ID in the request. It belongs to the category Broken Access Control.
- Authentication = Who are you? . Authorization = What are you allowed to do ? .

- Privilege escalation: horizontal = reach another user's data at the same
  level (IDOR); vertical = climb to higher permissions (e.g. user → admin).
- Lab: TryHackMe OWASP 2025 room, found the millionaire via IDOR (changing ?id=).

**What I practiced:**
- the tryhackme room OWASP Top 10 2025: IAAA Failures (Broken Access Control)

**What confused me:**
- ______

**Tomorrow:**
- Day 3: follow one HTTP request from Angular to Spring Boot.