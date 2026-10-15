# Day 3: Follow one HTTP request

**What I learned:**
- An HTTP request (what goes out) has: method, path/URL, version, headers
  (plus a body for POST/PUT).
- An HTTP response (what comes back) has: status line, headers, body.
  (Content-Type and Content-Length are just examples of headers.)
- Status is a RESPONSE part, not a request part: the request says what I want,
  the response says what happened.
- Status code families:
  - 2xx = success (200 OK)
  - 3xx = redirect (go look elsewhere)
  - 4xx = client fault (my request is wrong)
  - 5xx = server fault (the backend broke)
- 401 = "I don't know who you are" (not authenticated).
  403 = "I know you, but you can't have this" (authenticated, not authorized).
- A correct app would have returned 403 on yesterday's IDOR; the bug was
  returning 200 and handing over the data.

**What I practiced:**
- curl -v on httpbin.org: read the > (sent) and < (received) lines.
- DevTools Network tab: inspected a request's method, path, and status code.
- Noticed the response leaked my public IP (origin) and the server version
  (Server: gunicorn/19.9.0), which is useful info for an attacker.

**What confused me:**
- Mixed up "status" as a request part at first; it's a response part.

**Tomorrow:**
- Day 4: wire an LLM API into a Spring Boot endpoint.