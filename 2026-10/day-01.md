# Day 1: SQL injection

**What I learned:**
- SQLi happens when user input is concatenated into the SQL string, so the
  database can't tell data from code.
- `' OR 1=1--` closes the text value, makes the condition always true, and
  comments out the rest of the query.
- Fix: parameterized queries (`?` placeholders). Data and code travel in
  separate channels, so input can never become code.
- Blacklisting bad characters doesn't work; attackers bypass it.

**What I practiced:**
- PortSwigger lab: retrieved hidden (unreleased) products via
  `category=Lifestyle' OR 1=1--`.

**What confused me:**
- (your notes)

**Tomorrow:**
- Day 2: OWASP Top 10 overview.

