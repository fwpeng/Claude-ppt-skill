# CLAUDE.md

## Project Identity
This repository is a reusable Claude Code skill for generating PowerPoint presentations based on user-defined PPT templates.

The main goal of this project is to reduce repeated prompting, save tokens, and make Claude Code generate presentation-ready PPT files that follow the user's own template style.

This is not a general PPT generator.

This is a template-driven PPT skill.

---

## Core Objective
Claude should help generate PPT files by following existing templates and template rules.

The system should:
- reuse predefined PPT templates
- preserve the user's visual style
- reduce repeated style instructions
- minimize token usage
- generate editable PowerPoint files
- avoid unnecessary manual modification by the user

---

## Priority Rules
When generating or editing PPT files, Claude must follow this priority order:

1. User's direct instruction
2. Existing PPT template file
3. Template rule file
4. Project rules in this CLAUDE.md
5. General presentation design best practices

Claude should not freely invent a new visual style unless explicitly requested.

---

## Repository Structure
```text
Claude-ppt-skill/
│
├── README.md
├── CLAUDE.md
├── LICENSE
├── .gitignore
│
├── prompts/
│   ├── system.md
│   ├── generate_ppt.md
│   └── rewrite_slide.md
│
├── templates/
│   ├── business/
│   ├── academic/
│   └── minimal/
│
├── template_rules/
│   ├── business.md
│   ├── academic.md
│   └── minimal.md
│
├── examples/
│
├── src/
│
├── output/
│
└── assets/
```

---

## Template System
All PPT generation in this repository must follow a template-driven workflow.

PPT templates are stored in:
```text
templates/
```

Template rule files are stored in:
```text
template_rules/
```

Each template should have a matching rule file.

Example:
```text
templates/business/business_template.pptx
template_rules/business.md
```

Claude should always read the matching template rule file before generating slides.

---

## Template Usage Rules
Claude must:
- preserve the template's visual identity
- preserve layout consistency
- preserve color consistency
- preserve typography consistency
- reuse existing slide layouts whenever possible
- avoid arbitrary redesigns
- avoid random visual styles
- avoid inconsistent spacing
- avoid changing title hierarchy
- avoid overloading slides with text

The PPT template is the primary source of visual truth.

If the template contains title slides, section divider slides, content slides, chart slides, summary slides, or Q&A slides, Claude should reuse those layout types appropriately.

---

## Default Presentation Rules
Unless overridden by template rules:
- use 16:9 widescreen layout
- use concise slide content
- use modern minimal design
- maintain clean and professional appearance
- keep strong visual hierarchy
- use consistent title placement
- use consistent margins and spacing
- maximum 5 bullet points per slide
- avoid long paragraphs
- prefer diagrams, charts, icons, and structured layouts over dense text
- use speaker notes only when useful

---

## Content Rules
Generated content should be:
- clear
- structured
- concise
- presentation-ready
- easy to edit
- visually scannable
- suitable for direct use

Claude should avoid:
- vague bullet points
- excessive explanations
- repeated content
- large text blocks
- unnecessary decorative elements
- overloaded slides
- inconsistent terminology

---

## Recommended Slide Structure
For most presentations, use this structure:

1. Title slide
2. Agenda / Overview
3. Background / Context
4. Main content sections
5. Key findings / Insights
6. Recommendation / Solution
7. Summary
8. Q&A

Claude may adjust the structure based on the user's task, target audience, and selected template.

---

## Workflow
When asked to generate a PPT, Claude should follow this workflow:

1. Identify the user's topic and goal
2. Identify the target audience
3. Select the most appropriate template
4. Read the matching template rule file
5. Generate a slide outline
6. Generate slide content
7. Apply the selected PPT template
8. Export the final editable PPTX file
9. Save the generated file to `output/`
10. Provide a concise summary of the generated file

Claude should avoid lengthy explanations unless the user explicitly asks for them.

---

## Token Optimization Rules
This repository exists to minimize token usage.

Claude should:
- avoid repeating project rules in normal responses
- avoid restating obvious instructions
- reuse existing prompts and template rules
- reuse existing PPT templates
- avoid regenerating unchanged slides
- produce compact but complete output
- ask only necessary clarification questions
- use file references instead of repeating long content
- keep explanations short unless the user asks for details
- directly generate files or code when possible

When possible, Claude should say what it will do and then produce the needed file, code, or output directly.

---

## Coding Rules
When writing code for this project:
- use Python
- prefer `python-pptx`
- keep code modular
- avoid hardcoded values when possible
- use clear function names
- separate content generation from template application
- separate style extraction from slide generation
- keep reusable logic in `src/`
- save generated PPT files in `output/`
- avoid unnecessary comments
- write code that is easy for Claude Code to modify later

Recommended source files:
```text
src/generate_ppt.py
src/apply_template.py
src/extract_style.py
src/utils.py
```

---

## File Naming Rules
Use clear and descriptive file names.

Good examples:
```text
templates/business/business_template.pptx
templates/academic/academic_template.pptx
template_rules/business.md
template_rules/academic.md
output/ai_agent_report.pptx
examples/startup_pitch_demo.pptx
```

Avoid vague names such as:
```text
test.pptx
new.pptx
final_final.pptx
demo1.pptx
```

---

## Prompt Files
Reusable prompt files are stored in:
```text
prompts/
```

Recommended prompt files:
```text
prompts/system.md
prompts/generate_ppt.md
prompts/rewrite_slide.md
```

The prompt files should help Claude perform repeated tasks with less token usage.

Claude should reuse these prompts instead of rewriting long instructions every time.

---

## Template Rule Files
Template rule files describe the visual rules of each PPT template.

Each rule file should define:
- color system
- typography
- layout rules
- title style
- body text style
- chart rules
- icon rules
- slide density
- preferred slide types
- forbidden styles

Example:
```text
template_rules/business.md
```

Claude should treat template rule files as the written design language of the PPT template.

---

## Assets
Reusable visual assets should be stored in:
```text
assets/
```

Possible asset folders:
```text
assets/icons/
assets/images/
assets/logos/
```

Claude should reuse existing assets when they match the selected template style.

---

## Examples
Example outputs should be stored in:
```text
examples/
```

Examples are used as reference cases for future PPT generation.

Good examples include:
```text
examples/sample_outline.md
examples/generated_demo.pptx
examples/before_after.md
```

Claude may use examples as few-shot references for style and structure.

---

## Output Expectations
Generated PPT files should:
- follow the selected template
- look presentation-ready
- require minimal manual editing
- preserve style consistency
- maintain clear slide hierarchy
- be editable in Microsoft PowerPoint
- support business, academic, and professional scenarios
- use the user's template as the visual source of truth

---

## Important Constraint
Claude should not treat PPT templates as optional.

The template is the source of truth for visual design.

If there is any conflict between:
- general design advice
- and the template style

the template style should always win.

Claude should only deviate from the template when the user explicitly requests it.

---

## User Preference
The user wants this skill to reduce repeated prompting and save tokens.

The user prefers template-based PPT generation so that future PPT files can be generated directly according to the user's own PPT templates with minimal manual editing.

Claude should prioritize automation, consistency, and token efficiency.

---

## Future Development Goals
Possible future improvements:
- automatic template style extraction
- markdown-to-PPT generation
- multiple template support
- chart generation
- icon library integration
- academic presentation mode
- business presentation mode
- consulting presentation mode
- startup pitch mode
- one-command PPT generation workflow
- automatic slide rewriting
- automatic slide polishing
- automatic speaker notes generation
