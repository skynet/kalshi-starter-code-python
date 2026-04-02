# FMV Gold Project Preferences

**Version:** 1.0  
**Last Updated:** April 1, 2026  
**Purpose:** Document project-specific preferences and rules for development workflow

---

## 📋 Overview

This document establishes working preferences for the FMV Gold project to optimize efficiency and clarity when working with Kombai and other LLMs.

---

## 🎯 Documentation Reading Rules

### **Rule: Selective Document Reading**

**Do NOT automatically read the following documentation files:**
- `DESIGN-BLOCKS.md`
- `BOOTSTRAP-REFERENCE.md`
- `KOMBAI-CAPABILITIES.md`

**ONLY read them if the engineer explicitly references them in the request.**

### **When to Read Them**

**Read DESIGN-BLOCKS.md when:**
```
"Create About page using: Hero, 3-Column Grid, Testimonials, Dark CTA"
(Block names referenced → read the doc)

"Check DESIGN-BLOCKS.md for available patterns"
(Explicitly asked)
```

**Read BOOTSTRAP-REFERENCE.md when:**
```
"See BOOTSTRAP-REFERENCE.md for button customization"
(Explicitly asked)

"How do I customize buttons (check BOOTSTRAP-REFERENCE.md)?"
(Explicitly referenced)
```

**Do NOT read them when:**
```
"Create an About page"
(No reference to docs → ask clarifying questions instead)

"Build a dashboard"
(No reference to docs → ask what blocks to use)
```

### **Rationale**

- Saves ~100-150 tokens per task by avoiding unnecessary doc reads
- Keeps workflow focused on task requirements
- Documentation serves as reference/reference material, not default reading
- Reduces token overhead while maintaining access to information when needed

---

## 💰 Token Optimization Strategy

### **Goal**
Minimize token usage by being selective about what I read, while maintaining access to comprehensive documentation when explicitly needed.

### **How It Works**

| Scenario | Action | Tokens Saved |
|----------|--------|--------------|
| "Create About page" | Ask clarifying questions | ~100-150 |
| "Create About page using Hero + Testimonials" | Reference docs if needed, implement | ~0-50 |
| "Check BOOTSTRAP-REFERENCE.md for X" | Read doc + implement | None (requested) |
| Iterative changes without doc reference | Ask questions, adjust | Varies |

### **Expected Outcome**

- **Per-task average:** 10-15% token savings through selective reading
- **Over 10 tasks:** ~1,500-2,000 token savings
- **Quality:** No reduction (docs available when referenced)

---

## 🗣️ Communication Expectations

### **Engineer Communication Style**

- Requests are brief and to the point
- May or may not reference documentation
- Clear intent communicated directly

### **Kombai Response Pattern**

- If intent is clear AND blocks are referenced → Implement directly
- If intent is clear BUT blocks NOT referenced → Ask which pattern to use
- Always respect explicit documentation references

---

## 🎨 Material Design Icons Preference

### **Rule: Always Ask About Icon Choice**

When creating pages, forms, components, or features that might benefit from icons, **always ask** whether to use **Material Design Icons** or create versions **without icons**.

### **When This Rule Applies**

Applies to requests for:
- ✅ Login/Register pages
- ✅ Form components
- ✅ Navigation elements
- ✅ Dashboards or data displays
- ✅ Feature cards or sections
- ✅ Any page with interactive elements

### **How to Ask**

**Good example:**
```
"Create a dashboard component. Should I use Material Design Icons or keep it icon-free?"
```

**What I'll do:**
1. Ask: "Material Design Icons or without icons?"
2. Wait for your preference
3. Create both versions OR just the preferred version
4. Provide links to live preview

### **Why This Matters**

| With Icons | Without Icons |
|-----------|--------------|
| More visual polish | Cleaner, minimal feel |
| Professional appearance | Focus on typography |
| 2000+ icon options | Smaller file size |
| Requires CDN | Faster loading |
| Premium/polished look | Modern simplicity |

### **Example Scenarios**

**You ask:** "Create a login page"  
**I ask:** "Material Design Icons or without?"  
**You can say:**
- "With Material Design Icons" → Get: `auth-with-material-icons.html`
- "Without icons" → Get: `auth-without-icons.html`
- "Both versions" → Get: Both files for comparison

---

## 📚 Documentation Purpose

### **DESIGN-BLOCKS.md**
**Purpose:** Reusable UI components and patterns for FMV Gold  
**Use:** Reference when building new pages, share with team, version control  
**When I Read:** Only when explicitly referenced

### **BOOTSTRAP-REFERENCE.md**
**Purpose:** Quick lookup of Bootstrap components used in project  
**Use:** Reference Bootstrap customizations, link to official docs  
**When I Read:** Only when explicitly referenced

### **KOMBAI-CAPABILITIES.md**
**Purpose:** Explain Kombai's strengths and limitations  
**Use:** Inform external LLMs about what Kombai can do, planning phase  
**When I Read:** Only when explicitly referenced

### **PROJECT-PREFERENCES.md** (This file)
**Purpose:** Document project-specific working rules  
**Use:** Establish clear expectations for development workflow  
**When I Read:** Always (foundational rules)

---

## ✅ Checklist for New Requests

When making a request, you can follow this checklist:

**If you want Kombai to reference docs:**
- [ ] Explicitly mention the document name
- [ ] Reference specific blocks/sections if applicable
- Example: "Create About page using DESIGN-BLOCKS.md blocks: Hero, Testimonials, Footer"

**If you DON'T want Kombai to read docs:**
- [ ] Just state the request normally
- [ ] Ask clarifying questions if needed
- Example: "Create an About page" → Kombai will ask "Which blocks?"

**If you're unsure:**
- [ ] It's okay to ask "Should I reference X doc?"
- [ ] Kombai will confirm preference

---

## 🔄 Workflow Summary

```
1. You make a request (with or without doc references)
2. If doc referenced → I read it + implement
3. If doc NOT referenced → I ask for clarification/blocks
4. You clarify (optionally referencing docs)
5. I implement
6. Done ✅

Total tokens saved: ~100-150 per task (if selective)
```

---

## 📝 When to Update This Document

Update PROJECT-PREFERENCES.md when:
- [ ] New documentation patterns are established
- [ ] New rules for workflow are created
- [ ] Preferences change based on project needs
- [ ] New team members need onboarding

**Frequency:** As needed (no scheduled review)

---

## 🎯 Key Takeaway

**"Make requests clear, reference docs explicitly when needed, let Kombai handle the rest."**

This keeps the workflow efficient and token-aware while maintaining full access to comprehensive documentation.

---

**Version History:**
- v1.1 (April 1, 2026) - Added Material Design Icons preference
- v1.0 (April 1, 2026) - Initial preferences established
