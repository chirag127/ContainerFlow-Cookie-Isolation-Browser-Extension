# 🚀 Pull Request Template: Apex Architecture Review

**Developer:** @[Your GitHub Handle]

## 🎯 PR Title Convention

Use descriptive, imperative titles formatted as:
`[FEATURE/FIX/REFACTOR/DOCS]: Concise summary of change (Context)`

*Example: `[FEATURE]: Implement Domain-Specific Cookie Storage API (WebExtensions)`*

---

## 📖 1. Description & Rationale (BLUF)

**Briefly summarize the goal of this Pull Request.** Why is this change necessary? What problem does it solve or what capability does it introduce?

[Detailed Explanation Here]

---

## ✅ 2. Verification & Testing Checklist

**All changes MUST be verifiable against the established architecture and testing standards.**

- [ ] **Local Verification:** Have you run the application/extension locally and manually confirmed the behavior?
- [ ] **Unit Tests:** Have relevant unit tests been added or updated (Utilizing Vitest/Playwright conventions)?
- [ ] **E2E Tests:** Are new E2E scenarios covered by Playwright scripts if applicable to user journeys?
- [ ] **Linter/Formatter Check:** Did you run `npx @biomejs/biome check --apply .` (or relevant stack command) before committing?
- [ ] **Security Scan:** Have you reviewed for any new direct dependencies or potential XSS/CSRF vectors?

---

## 🧠 3. Architectural Alignment (APEX MANDATE)

Reference the architectural patterns defined in `AGENTS.md`. How does this PR maintain or enforce:

1.  **SOLID Principles?** (Especially Single Responsibility and Dependency Inversion for JS architecture)
2.  **DRY Principle?** (Avoidance of code duplication in handling container logic)
3.  **YAGNI?** (Ensuring only necessary functionality is built)

**Specific Architectural Component Affected:**

*e.g., `src/background/cookieManager.ts`, `src/popup/uiController.ts`*

---

## 🔗 4. Linked Issues / Context

Closes #[Issue Number]
Fixes #[Issue Number]
Relates to #[Issue Number]

---

## 📸 5. Visual Proof (If applicable to UI/UX)

*(If this PR modifies the user interface or behavior, include screenshots or recording links here.)*

---

## ⚠️ Self-Review Notes for Reviewer

*Highlight any complex logic, potential edge cases, or areas where you specifically seek deep architectural feedback.* 

**Example:** "Review the asynchronous handling in `containerService.ts`—I suspect race conditions might occur during rapid tab switching under high load."
