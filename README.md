# Activate Labs

Self-serve AI workshops that scale what live demos can't.

## What This Is

I've run hundreds of live AI demos. They work—people leave with something real. But they don't scale.

This repository contains **Activate** content: browser-based, self-serve labs that walk you through building practical AI solutions in 20-60 minutes. No coding required. No server setup. No IT tickets.

These labs are designed to be **white-label ready**. If you're running AI adoption programs at your organization, take them. Rebrand them. The goal was never to hoard this stuff—it's to get more people past the "I don't know where to start" barrier.

## Content Framework

This repo is part of a three-tier content system:

| Type | Purpose | Location |
|------|---------|----------|
| **Narrate** | Stories, insights, lessons learned | [landtiser.com/blog](https://landtiser.com/blog) |
| **Curate** | External resources with commentary | [landtiser.com/blog](https://landtiser.com/blog) |
| **Activate** | Hands-on labs you can complete now | This repo |

**Activate** labs are designed to follow **Narrate** stories (understanding why) and **Curate** resources (seeing what's possible), giving you a complete learning path from concept to implementation.

## Available Labs

### Lab #1: The Bio Builder
**Duration:** 20 minutes
**Difficulty:** Beginner
**Platform:** Microsoft Copilot Studio Lite

Build an AI agent that customizes your professional bio for specific sales opportunities. Useful without being high-stakes—you're not automating client deliverables, just making the "ugh, I need to tweak my bio again" task disappear.

**Why this lab first?** Your first agent should solve a real annoyance, not aim to revolutionize an industry.

[Launch Lab →](https://landtiser.com/lab/bio-customizer.html) | [Read the story](https://landtiser.com/bio-customizer-agent)

---

### Lab #2: Master Your Inbox with Copilot Prioritize

**Duration:** 45 minutes  
**Difficulty:** Beginner  
**Platform:** Microsoft Outlook (Copilot license required)

Configure Outlook's AI prioritization to actually work for you. You'll set up custom rules for what counts as high priority (and more usefully, low priority), configure the mobile experience, and learn how to refine your instructions as Copilot learns your patterns.

**Why this lab?** Lab #1 was about building an agent. This one is about using AI that's already in your tools. Both skills matter—and they're completely different muscles.

[Launch Lab →](https://landtiser.com/lab/copilot-prioritize.html) | [Read the story](https://landtiser.com/copilot-prioritize-lab)

---

## How to Use These Labs

### As a Learner
1. Click any lab link above
2. Follow the step-by-step instructions
3. Build something real in 20-60 minutes
4. Actually use what you built

### As an Adoption Lead
1. Fork this repository
2. Customize the white-label sections (see Customization Guide below)
3. Host on GitHub Pages (free) or your internal network
4. Share the lab URLs with your teams
5. Watch people build confidence through doing

### As a Contributor
See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on submitting new labs or improvements.

---

## Customization Guide

Each lab is built as a **single HTML file** with embedded CSS and JavaScript—no build process, no dependencies. This makes white-labeling straightforward.

### What to Customize

Every lab includes clearly marked white-label sections:

```html
<!-- ═══════════════════════════════════════════════════════════════
     WHITE-LABEL INSTRUCTIONS

     To customize this lab for your organization:

     1. Find/Replace "Chris Landtiser" with your name/brand
     2. Find/Replace "landtiser.com" with your website
     3. Optionally update colors in the :root CSS variables

     Look for <!-- YOUR BRAND --> comments for key locations
     ═══════════════════════════════════════════════════════════════ -->
```

### Key Customization Points

1. **Header Badge** (line ~715): Your organization name
2. **Footer Brand** (line ~1073): Your branding and website
3. **Completion Links** (line ~1056): Where learners should go next
4. **Color Palette** (line ~27): Optional—update CSS variables to match your brand

### Example: Rebranding for "Contoso Corp"

```bash
# In any lab HTML file:
Find: "Chris Landtiser"
Replace: "Contoso Corp Learning Team"

Find: "landtiser.com"
Replace: "contoso.com/ai-academy"
```

That's it. The lab is now branded for Contoso.

---

## Hosting Options

### Option 1: GitHub Pages (Free, Public)
1. Fork this repository
2. Go to Settings → Pages
3. Select "main" branch and "/" root
4. Your labs will be live at `yourname.github.io/activate-labs`

### Option 2: Internal Network
1. Download any lab HTML file
2. Upload to your SharePoint, intranet, or file server
3. Share the link—no server configuration needed

### Option 3: Custom Domain
1. Follow GitHub Pages setup
2. Add a CNAME file with your domain
3. Configure DNS to point to GitHub Pages
4. Labs live at `labs.yourdomain.com`

---

## Lab Design Philosophy

Every lab in this repository follows these principles:

1. **Solve a Real Annoyance**
   No "build a chatbot because it's cool." Every lab addresses an actual workplace frustration.

2. **Low Stakes, High Learning**
   You're not touching production systems or sensitive data. You're building something useful in a safe sandbox.

3. **Browser-Based**
   No installations, no CLI commands, no "works on my machine" problems. Just open and go.

4. **20-60 Minutes**
   Respect people's time. If it takes longer, it should be multiple labs.

5. **Beginner-Friendly**
   Assume zero AI experience. Explain jargon. Include troubleshooting.

6. **White-Label Ready**
   Clear customization points. No hardcoded assumptions. Make it yours.

---

## Technical Architecture

### Why Single-File HTML?

Each lab is a self-contained HTML file with embedded CSS and JavaScript. This seems old-school, but it's intentional:

- **Zero Dependencies**: No npm, no build process, no version conflicts
- **Easy Hosting**: Drop it anywhere that serves HTML
- **Simple Customization**: Find/replace in one file beats hunting across directories
- **Long-Term Stability**: No framework churn, no broken builds in 2 years
- **Offline-Capable**: Download once, run anywhere

### Design System

Labs use a consistent design system with CSS custom properties:

```css
:root {
  --voyager-blue: #003366;
  --voyager-teal: #008080;
  --voyager-gold: #B8860B;
  /* ... */
}
```

**Voyager Palette:** Named for the furthest-traveled human-made objects—because good labs should take learners somewhere new.

### Progressive Enhancement

- Works without JavaScript (progress tracker won't update, but content is accessible)
- Mobile-responsive from the start
- Print-friendly for offline reference
- Accessible (semantic HTML, ARIA labels, keyboard navigation)

---

## Contributing

I built these labs for live workshops with hundreds of attendees. They've been debugged by:
- Day-one learners who've never heard of AI
- IT leads who implement at scale
- Skeptics who just wanted to see if this AI stuff was real

But they can always be better. Contributions welcome:

- **New Labs**: Follow the template structure, submit a PR
- **Improvements**: Clearer instructions, better troubleshooting, UX fixes
- **Translations**: Help make these accessible to non-English speakers
- **Bug Reports**: If something doesn't work, open an issue

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

---

## Support & Community

- **Questions?** Open a [GitHub Discussion](../../discussions)
- **Bug Reports:** File an [Issue](../../issues)
- **Want to chat?** Find me on [LinkedIn](https://linkedin.com/in/landtiser)
- **Read the stories:** [landtiser.com](https://landtiser.com)

---

## The Bigger Picture

These labs are **Activate** content—hands-on learning that follows **Narrate** (stories) and **Curate** (resources).

### Why This Framework Matters

Most AI content falls into two camps:
1. **Inspirational but Vague**: "AI will change everything!" (Okay, but *how*?)
2. **Technical but Intimidating**: "Fine-tune your LLM with this 47-step process..." (I just wanted to try something.)

The Narrate-Curate-Activate framework bridges this gap:

- **Narrate** gives you the *why* and the *context*
  (Stories from real implementations, lessons learned, honest reflections)

- **Curate** shows you *what's possible*
  (Vetted resources, expert takes, tools worth your time)

- **Activate** teaches you *how to do it*
  (Hands-on labs, 20-60 minutes, something you can actually use)

This repository is the **Activate** layer. It's where understanding becomes action.

---

## Values

The principles that guide this work:

### Start with Problems, Not Solutions
Every lab addresses a real workplace annoyance. No "build AI because it's trendy."

### Test, Learn, Scale
Small pilots with clear success metrics. Labs let you test ideas safely before organization-wide rollouts.

### Human-Centric Design
AI should reduce friction, not create it. Every lab considers the person using it—their workflow, their concerns, their actual needs.

### Quality Over Quantity
The goal isn't to multiply sheer productivity—it's to create space for better thinking and meaningful contributions.

### Augment, Never Replace
AI provides insights; people make decisions based on context, ethics, and judgment no algorithm can match.

### Tools for Everyone
AI shouldn't live within the IT department. When we put innovation tools directly in teams' hands, they solve real problems we never even knew existed.

---

## What's Next

Here's what I've learned from all those live demos: **the hardest part isn't teaching people how to build agents. It's convincing them they're allowed to try.**

You are. Go build something.
