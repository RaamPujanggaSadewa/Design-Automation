# Vibecoding

A UI/UX designer workflow for creating designs and code by teaming up with AI using different reference sources. The vibe? Let AI learn from what you show it, then create something fresh.

---

## Flow 1: Internet Reference

**The Vibe:** Find inspiration anywhere online, have AI extract it, and use it to guide your design.

**What You Need:**
- A reference image (Dribbble, Behance, Pinterest, whatever)
- (Optional but way better) An existing `design.md` template to show AI the format you like

**The Steps:**
1. Search for reference designs online
2. Upload the image to AI and ask it to extract all the info
3. AI creates a `design.md` file (looks better if you provide an example like [design2.md](./design2.md))
4. Create a `design-brief.md` that explains:
   - What you're building (landing page, dashboard, etc.)
   - What should be in it (sections, features, components)
   - Do's and don'ts
   - Any other vibes you want to set
5. Give both files to AI and ask it to create the design/code

**Pro Tip:** If you already have a `designbrief.md` example (like [this one](./designbrief.md)), show it to AI. It makes everything way cleaner.

---

## Flow 2: Design System Reference

**The Vibe:** Use an existing design system from big companies. Skip the manual extraction—just grab the system that fits your vibe.

**What You Need:**
- A design system MD file from [getdesign.md](https://getdesign.md) (Apple, Airtable, Airbnb, etc.)
- A `design-brief.md` explaining what you want to build

**The Steps:**
1. Find and download a design system MD from [getdesign.md](https://getdesign.md)
2. Create a `design-brief.md` (use the template approach from Flow 1 if you want)
3. Put both files together and ask AI to create what you need following that design system

**Different from Flow 1?** Yeah—you're not extracting from images. The system is already documented, you just apply it.

---

## Flow 3: Live Product Code Reference

**The Vibe:** Learn from existing code, understand its patterns, then create something new that feels like it belongs.

**What You Need:**
- A GitHub repo of a live product
- Access to your local dev environment
- The ability to clone specific parts (like a landing page folder)

**The Steps:**
1. Create/use your GitHub account
2. Clone the repo or download a specific folder (e.g., the landing page directory)
3. Open the code in your editor (VS Code, whatever)
4. Show the code to AI and ask it to understand the patterns
5. Tell AI to create something new while keeping the same style and code patterns
6. AI creates the design/code that matches your existing product's vibe

**The Magic:** AI already knows how your product works, so it can create things that actually fit.

---

## Flow 4: Figma Reference

**The Vibe:** Figma designs → AI reads them → Code appears. But first, you gotta set up the connection.

**What You Need:**
- A Figma design file
- Talk to Figma MCP set up (follow the guide below)
- AI connected to Figma

**The Setup:**
→ Check out [Figma Guide](https://figma-guide-toec.vercel.app/) for the full setup details. It walks you through everything.

**The Steps:**
1. Set up your Figma connection (see the guide above)
2. Have your Figma design ready
3. Ask AI to connect to Figma and read your design
4. AI learns the design and creates the code

---

## Quick Reference

| Flow | Source | Speed | Best For |
|------|--------|-------|----------|
| 1 | Internet images | Medium | One-off designs, getting inspired |
| 2 | Design systems | Fast | Following established systems, consistency |
| 3 | Live product code | Medium | New features that match your existing product |
| 4 | Figma | Fast (once set up) | Designs you've already made in Figma |

---

## Templates to Use

- **Design System Template:** [design2.md](./design2.md) - Shows color, typography, spacing, components
- **Design Brief Template:** [designbrief.md](./designbrief.md) - Project overview, flows, users, constraints, goals

---

## Results (All One-Shot Prompts)

These are working examples from each flow. All created with single prompts—no fine-tuning, no iterations. Just AI understanding the reference and creating the code.

### Flow 1: Internet Reference
**Result:** NomadNest 95 Landing Page  
**Based on:** Windows 95 design aesthetic from Dribbble/Pinterest  
→ [View Result](./index2.html)  
*Single prompt extracted the design vibe and generated the full HTML*

### Flow 2: Design System Reference  
**Result:** NomadNest Landing Page (Airbnb Design System)  
**Based on:** Airbnb's design system from [getdesign.md](https://getdesign.md)  
→ [View Result](./index.html)  
*AI applied Airbnb's design tokens and patterns to create the landing page*

### Flow 3: Live Product Code Reference
**Result:** Share Checkout Link Component (Vue)  
**Based on:** Existing live product code patterns  
→ [View Code](./share.vue)  
*AI learned the existing code style and created a new component that matches*

### Flow 4: Figma Reference
**Result:** Onboarding Mobile Screen  
**Based on:** Figma design using Talk to Figma MCP  
→ [View Result](./index3.html)  
*AI read Figma designs and generated the interactive HTML*

---

## The Takeaway

One good reference = one good prompt = working output. No need for multiple iterations or fine-tuning. The skill is knowing *what* to show the AI, not having to explain it in 100 words.
