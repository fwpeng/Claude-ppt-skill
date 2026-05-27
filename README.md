# Claude PPT Skill

A reusable Claude Code skill for generating PowerPoint presentations based on user-defined PPT templates.

This project is designed to reduce repeated prompting, save tokens, and make Claude Code generate presentation-ready PPT files that follow the user's own template style.

## Purpose

This repository is not a general PPT generator.

It is a template-driven PPT skill that helps Claude Code generate PowerPoint files using predefined templates, rules, and reusable prompts.

## Features

- Template-based PPT generation
- User-defined PPT style preservation
- Token-saving workflow
- Reusable prompt system
- Editable PowerPoint output
- Business presentation template support

## Repository Structure

```text
Claude-ppt-skill/
├── CLAUDE.md
├── README.md
├── LICENSE
├── .gitignore
├── output/
│   └── .gitkeep
├── prompts/
│   └── system.md
├── template_rules/
│   └── business.md
└── templates/
    └── business/
        └── PPT_template.pptx
```

## How It Works

Claude Code should follow this workflow:

1. Read `CLAUDE.md`
2. Read the selected template rule file in `template_rules/`
3. Use the matching PPT template in `templates/`
4. Generate slide outline and content
5. Apply the template style
6. Save the final PPTX file to `output/`

## Default Template

The current default template is:

```text
templates/business/PPT_template.pptx
```

The matching template rule file is:

```text
template_rules/business.md
```

## Usage Example

Example request:

```text
Use the business template to generate a 10-slide PPT about AI agents.
```

Claude Code should then:

- follow `CLAUDE.md`
- use `template_rules/business.md`
- apply `templates/business/PPT_template.pptx`
- save the generated PPTX file in `output/`

## Design Principle

The PPT template is the source of truth for visual design.

Claude should not freely invent a new visual style unless explicitly requested.

## Token Saving

This skill reduces token usage by storing repeated instructions in project files instead of asking the user to repeat them every time.

Stored reusable context includes:

- project rules
- template rules
- system prompt
- PPT template path
- output workflow

## Current Status

Basic framework completed.

Included:

- `CLAUDE.md`
- `prompts/system.md`
- `template_rules/business.md`
- `templates/business/PPT_template.pptx`
- `output/.gitkeep`

## Future Plans

- Add more PPT templates
- Add academic template mode
- Add consulting template mode
- Add automatic PPT generation script
- Add markdown-to-PPT workflow
- Add automatic style extraction
