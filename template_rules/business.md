# Business Template Rules

## Template Identity
This template is the default business PPT template for this repository.

Claude must use this template when the user asks for:
- business presentations
- project reports
- company reports
- strategy presentations
- consulting-style slides
- pitch decks
- professional summaries

---

## Design Goal
The goal of this template is to create professional, clean, and presentation-ready business slides.

The design should feel:
- modern
- structured
- clear
- concise
- executive-friendly
- easy to edit

---

## Template Preservation Rules
This template must be used by copying existing slides rather than recreating the design from scratch.

Claude should:
- duplicate template slides whenever possible
- preserve original background graphics
- preserve original layout structure
- preserve original title and body positions
- preserve original colors, fonts, and spacing
- preserve decorative shapes, logos, footer elements, and non-text visual elements
- replace only the text content needed for the new presentation
- keep the original visual hierarchy of the template

Claude should not:
- create new blank slides
- use default PowerPoint layouts
- manually rebuild backgrounds
- remove decorative elements
- change the visual identity of the template
- invent new layouts when a suitable template slide already exists
- redraw the design with Python unless explicitly required

---

## Visual Style
Claude should follow these visual principles:
- clean layout
- strong alignment
- clear hierarchy
- enough whitespace
- minimal decoration
- consistent page structure
- professional business tone

Avoid:
- childish design
- colorful random styles
- excessive decoration
- crowded slides
- inconsistent fonts
- inconsistent spacing

---

## Slide Density
Each slide should focus on one main idea.

Default rules:
- maximum 4 bullet points per slide
- maximum 1 main chart or diagram per slide
- avoid paragraphs
- prefer short phrases
- use keywords instead of long sentences

---

## Typography
Claude should preserve the typography style of the PPT template.

General rules:
- use large titles
- use concise body text
- keep title hierarchy consistent
- avoid too many font sizes
- avoid decorative fonts
- avoid excessive bold text

---

## Layout Rules
Claude should reuse existing layouts from the PPT template whenever possible.

Preferred layouts:
- title slide
- section divider slide
- two-column content slide
- key insight slide
- chart slide
- comparison slide
- timeline slide
- summary slide
- Q&A slide

Avoid:
- manually inventing random layouts
- placing text too close to page edges
- inconsistent alignment
- unbalanced slide composition
- using blank default PowerPoint pages
- rebuilding the template layout from scratch

---

## Color Rules
Claude should preserve the color system of the selected PPT template.

If the exact template colors are unknown, use a professional business color system:
- primary color: dark blue or navy
- secondary color: white or light gray
- accent color: blue, cyan, or muted orange
- avoid overly bright colors
- avoid using too many colors on one slide

---

## Chart Rules
When charts are needed:
- prefer bar charts, line charts, and simple comparison charts
- avoid unnecessary 3D charts
- avoid overly complex chart decorations
- keep chart labels readable
- use concise chart titles
- highlight the key insight clearly

If the template already contains a chart slide, Claude should duplicate that chart slide and replace the chart data or labels while preserving the original layout and style.

---

## Icon and Image Rules
Icons and images should support the content, not decorate randomly.

Claude should:
- use simple line icons when appropriate
- keep icon style consistent
- use images only when they improve understanding
- avoid low-quality images
- avoid unrelated stock-photo style images

Claude should preserve existing template icons and images unless the user explicitly asks to replace them.

---

## Content Tone
The writing style should be:
- professional
- concise
- direct
- structured
- suitable for business readers

Avoid:
- casual language
- vague claims
- long explanations
- repeated points

---

## Default Slide Structure
For business presentations, use this structure by default:

1. Cover
2. Executive Summary
3. Background / Context
4. Key Issues
5. Analysis
6. Recommendation
7. Implementation Plan
8. Expected Impact
9. Summary
10. Q&A

Claude may adjust the structure based on the user's request.

---

## Generation Workflow
When generating a business PPT with this template, Claude should:

1. Open `templates/business/PPT_template.pptx`.
2. Identify reusable template slides.
3. Select the most suitable slide type for each new slide.
4. Duplicate existing template slides instead of creating blank slides.
5. Replace only editable text, chart labels, and necessary content.
6. Preserve background, layout, decorations, logos, footers, fonts, colors, and spacing.
7. Save the final file to `output/`.

If the template does not contain enough reusable slide types, Claude should ask the user to provide more sample slides instead of inventing a new design.
