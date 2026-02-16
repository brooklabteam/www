# Plan: Consolidate e2m2.org and coding4conservation.org into brooklab.org

## Current State

**brooklab.org** is a Jekyll 4.3.3 site deployed on Netlify. It already has a `/programs` page that links out to e2m2.org and coding4conservation.org as external sites. The site uses Bootstrap 5, Plausible analytics, and the UC Berkeley color scheme.

**e2m2.org** — Ecological & Epidemiological Modeling in Madagascar. An 8-day intensive workshop for Malagasy graduate students. The site contains:
- Homepage with program overview and application info
- Yearly syllabi under `/archives/YYYY` (at least 2022, 2024, 2025)
- Lecture PDFs and homework submissions under `/assets/YYYY/`
- Faculty/instructor information

**coding4conservation.org** — A year-long R-based mentorship program for Malagasy students. The site contains:
- Homepage with program overview and application info
- `/syllabus` — Training themes by week, mentor/mentee goals
- `/mentors` — Mentor bios and photos
- `/students` — Student cohort profiles and projects
- `/preparation` — Pre-program setup instructions
- Lecture PDFs under `/assets/lectures/`

---

## Proposed URL Structure

All program content lives under `/programs/` on brooklab.org:

```
/programs                          ← index (existing, update cards)
/programs/e2m2                     ← E2M2 landing page (overview, apply, contact)
/programs/e2m2/2025                ← 2025 syllabus & schedule
/programs/e2m2/2024                ← 2024 syllabus & schedule
/programs/e2m2/2022                ← 2022 syllabus & schedule
/programs/coding4conservation      ← C4C landing page (overview, apply, contact)
/programs/coding4conservation/syllabus    ← Current syllabus
/programs/coding4conservation/mentors     ← Mentor bios
/programs/coding4conservation/students    ← Student cohort & projects
/programs/coding4conservation/preparation ← Pre-program setup
```

Assets would go into corresponding subdirectories:
```
/programs/e2m2-assets/             ← E2M2 lectures, PDFs, images
/programs/c4c-assets/              ← C4C lectures, PDFs, images
```

---

## Implementation Steps

### Phase 1: Scaffold the new pages on brooklab.org

1. **Create `/programs/e2m2.md`** — E2M2 landing page with:
   - Program description and goals
   - Application information and timeline
   - Faculty/instructor list
   - Links to yearly archive pages
   - Contact info

2. **Create yearly archive pages** — e.g., `/programs/e2m2/2025.md`, `/programs/e2m2/2024.md`, etc., each containing:
   - Syllabus / daily schedule
   - Links to lecture materials (PDFs)
   - Final symposium info

3. **Create `/programs/coding4conservation.md`** — C4C landing page with:
   - Program description, goals, and eligibility
   - Application info
   - Links to sub-pages (syllabus, mentors, students, preparation)

4. **Create C4C sub-pages:**
   - `/programs/coding4conservation/syllabus.md`
   - `/programs/coding4conservation/mentors.md`
   - `/programs/coding4conservation/students.md`
   - `/programs/coding4conservation/preparation.md`

5. **Copy assets** — Migrate lecture PDFs, images, and other static files into `/programs/e2m2-assets/` and `/programs/c4c-assets/`.

6. **Update `/programs.md`** — Change the E2M2 and C4C card links from external URLs to internal paths (`/programs/e2m2` and `/programs/coding4conservation`).

### Phase 2: Navigation and discoverability

7. **Add sub-navigation within program pages** — Each program landing page should include a small nav or linked list to its sub-pages (e.g., Syllabus | Mentors | Students for C4C).

8. **No changes to the main navbar** — The top-level "Programs" link already exists and leads to `/programs`, which serves as the index. No new top-level nav items needed.

### Phase 3: Redirects from old domains

9. **Set up domain redirects** — Configure e2m2.org and coding4conservation.org to redirect to their new locations on brooklab.org. Options:
   - **Option A (Recommended): Netlify redirects on the old domains** — If both old sites are also on Netlify, add `_redirects` rules that map old paths to new brooklab.org paths (e.g., `/* https://brooklab.org/programs/e2m2/:splat 301!`).
   - **Option B: DNS-level redirect** — If using Cloudflare for DNS on both domains, use Cloudflare Page Rules or Bulk Redirects to forward all traffic.
   - **Option C: Keep old domains as thin redirect sites** — Replace site content with a simple `index.html` that does a `<meta>` refresh or JS redirect, plus a `_redirects` file.

   Path-specific redirects to preserve:
   ```
   e2m2.org/                    → brooklab.org/programs/e2m2
   e2m2.org/archives/2025       → brooklab.org/programs/e2m2/2025
   e2m2.org/archives/2024       → brooklab.org/programs/e2m2/2024
   e2m2.org/archives/2022       → brooklab.org/programs/e2m2/2022
   coding4conservation.org/             → brooklab.org/programs/coding4conservation
   coding4conservation.org/syllabus     → brooklab.org/programs/coding4conservation/syllabus
   coding4conservation.org/mentors      → brooklab.org/programs/coding4conservation/mentors
   coding4conservation.org/students     → brooklab.org/programs/coding4conservation/students
   coding4conservation.org/preparation  → brooklab.org/programs/coding4conservation/preparation
   ```

### Phase 4: Cleanup

10. **Update any cross-references** — Search the brooklab.org codebase for any remaining references to e2m2.org or coding4conservation.org (blog posts, etc.) and update them to internal links.

11. **Test all redirects and links** — Run `html-proofer` (already in the build pipeline) to verify no broken links.

12. **Update SEO metadata** — Ensure each new page has appropriate `title`, `description`, and Open Graph metadata.

---

## Content Migration Checklist

### E2M2 content to migrate:
- [ ] Homepage text (program overview, eligibility, application info)
- [ ] 2025 syllabus and schedule
- [ ] 2024 syllabus and schedule
- [ ] 2022 syllabus and schedule
- [ ] Lecture PDFs and materials (per year)
- [ ] Faculty/instructor bios
- [ ] Images and logos

### Coding 4 Conservation content to migrate:
- [ ] Homepage text (program overview, eligibility, application info)
- [ ] Syllabus (training themes, weekly schedule, mentor/mentee goals)
- [ ] Mentor bios and photos
- [ ] Student profiles and project descriptions
- [ ] Preparation instructions
- [ ] Lecture PDFs

---

## Key Decisions Needed

1. **Content freshness**: Should all historical E2M2 archives be migrated, or only the most recent 2-3 years?
2. **Asset hosting**: Should lecture PDFs and large files continue to be hosted in the Git repo, or move to external storage (e.g., Google Drive links, university file hosting)?
3. **Domain retention**: Do you want to keep renewing e2m2.org and coding4conservation.org (as redirect-only domains), or let them expire eventually?
4. **Application forms**: Where do E2M2 and C4C applications currently live (Google Forms, etc.)? These links just need to be carried over to the new pages.
