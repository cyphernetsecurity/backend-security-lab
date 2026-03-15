# Backend Security Lab

Security investigations and backend security research focused on:

- Node.js ecosystems
- Dependency chain analysis
- File upload security
- API attack surfaces
- OSS vulnerability investigations

This repository documents technical investigations performed on real-world
backend systems and open-source projects.

---

## Investigations

### Strapi – fast-xml-parser dependency chain

Analysis of the dependency chain involving:

Strapi S3 Upload Provider  
→ AWS SDK (`@aws-sdk/client-s3`)  
→ `@aws-sdk/xml-builder`  
→ `fast-xml-parser`

Investigation performed to determine whether the vulnerability reported in
`fast-xml-parser` affects the current Strapi dependency tree.

Key tools used:

- `yarn why`
- `yarn npm audit`
- dependency tree analysis

Result: the current dependency tree resolves to `fast-xml-parser@5.3.6`
through `@aws-sdk/xml-builder`.

Further investigation may be required depending on release branches
or historical lockfile states.

---

## Focus Areas

Backend security topics explored in this lab:

- Secure file upload architectures
- Dependency vulnerability analysis
- Node.js security patterns
- API security testing
- Supply chain risk in JavaScript ecosystems

---

## Author

Gabriel Maheu  
Backend Security / API Security  
Founder — CypherNet Security
