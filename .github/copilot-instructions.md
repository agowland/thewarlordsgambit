# Copilot Instructions for The Warlord's Gambit

## Project Overview

**The Warlord's Gambit** is a campaign resource hub for a **Daggerheart** tabletop RPG campaign. Daggerheart is a narrative-driven heroic fantasy game blending D&D-style mechanics with collaborative storytelling. This repository organizes session materials, character questionnaires, rules references, and campaign documentation.

## Directory Structure & Key Files

- **Session Zero/** - Pre-campaign materials for Session Zero (player onboarding)
  - `Character Questionnaire.md` - Deep character creation questionnaire for players to develop character backstory and motivations
  - `What is Daggerheart.md` - Introduction to Daggerheart mechanics and core concepts
  - `Quick Reference.md` - Quick lookup for character traits, classes, ancestries, communities, and combat rules
  - `Rulebook Excerpts/` - PDF copies of official Daggerheart rulebook sections
- **README.md** - High-level project description
- **Session Notes/** - Directory for campaign notes or session recordings (TBD)

## Core Daggerheart Mechanics (Essential Knowledge)

### Fundamental System Principles

1. **Fiction-First Approach**: Rules serve the story, not vice versa. The GM and players act in good faith and focus on narrative over mechanics.
2. **Duality Dice**: All rolls use two differently-colored d12s:
   - One die represents **Hope**, the other represents **Fear**
   - The *sum* determines success/failure (meets/exceeds GM-set Difficulty)
   - The *higher die* determines advantage: Hope die > Fear die = player advantage (gain Hope); Fear die > Hope die = GM advantage (gain Fear)
3. **Mixed Outcomes**: Results aren't binary pass/fail—they're cinematic mixed successes (success with Hope, success with Fear, failure with Hope, failure with Fear)
4. **The Spotlight**: Narrative flows through the table by giving each player their moment in the spotlight one at a time

### Core Roll Types

- **Action Rolls**: Uncertain-outcome actions (attack, persuade, deceive). Generate Hope/Fear tokens based on outcome
  - Critical Success (both dice match, meet Difficulty): Gain Hope + clear Stress
  - Success with Hope: Get what you wanted + gain Hope
  - Success with Fear: Get what you wanted + GM gains Fear (consequence)
  - Failure with Hope: No success but gain Hope (silver lining)
  - Failure with Fear: Failure + things go very badly + GM gains Fear
- **Reaction Rolls**: Respond to attack/hazard (e.g., dodge). Don't generate Hope/Fear, no stress clearing

### Combat Differs from D&D

- **No Initiative**: Combat progresses narratively; GM decides when adversaries act
- **No Rounds**: Players describe actions in sequence, passing the spotlight
- **Spotlight-Driven**: Action flows naturally through narrative; GM makes moves when a player rolls Fear or fails
- **GM Moves**: When making an move, GM can show environmental reaction, ask questions, put players in tough spots, reveal secrets, introduce threats, use adversary Fear abilities, or offer dangerous bargains

### Character Building

- **Ancestries** (22 options): Define racial abilities (e.g., Dwarves gain +2 damage thresholds with Hope, Halflings give party Hope at session start)
- **Communities** (16 options): Define cultural upbringing and grant community abilities (e.g., Orderborne gain d20 as Hope die when embodying principles; Seaborne track Fear tokens for +1 roll bonuses)
- **Classes** (9 total with subclass variants): Each has unique combat and non-combat abilities
- **Experiences** (2 at creation): Each adds +2 modifier to relevant trait
- **Character Traits** (6): Agility, Strength, Finesse, Instinct, Presence, Knowledge—used for all rolls
- **Hit Points & Stress**: Physical (HP) and mental/emotional (Stress) damage; armor provides damage threshold

## Documentation Conventions

### Session Materials

When adding session materials:
- Use clear headings and organize by session (Session Zero, Session One, etc.)
- Character questionnaire responses should be compiled into a separate reference
- Rules clarifications should link to relevant section in Quick Reference
- Keep PDF copies of rulebook excerpts in `Session Zero/Rulebook Excerpts/` for easy reference

### Character Documentation

- Character questionnaires follow a two-tier structure: **The Basics** (required) and **The Deeps** (optional 1-3 answers for deeper exploration)
- Responses reveal character motivations, fears, hopes, and connections that the GM uses for spotlighting
- Personal connections between characters should be noted for facilitating group roleplay

### Rules References

The `Quick Reference.md` is the source of truth for:
- Trait definitions and usage
- All 9 classes and 2 subclasses per class
- All 22 ancestries with racial abilities
- All 16 communities with cultural abilities
- Experience mechanics
- Hit Points, Stress, Armor definitions
- Combat rules (no initiative, spotlight, GM moves, difficulty scale)

When referencing mechanics, link to relevant section in Quick Reference rather than duplicating content.

## Workflows & Best Practices

### When Writing Rules Clarifications

- Reference the Daggerheart Core Rulebook section (e.g., "Daggerheart_Core_Rulebook-5-20-2025-1.pdf, page X")
- Explain the **why** behind a ruling in terms of narrative and game feel, not just mechanics
- Follow the "Golden Rule": clarify that any rule can be modified with table consent if it better serves the story

### When Creating Session Notes

- Before Session Zero, ensure Character Questionnaires are distributed and responses compiled
- GM should review questionnaire answers to design spotlight moments that connect to character backstories
- Document which ancestries, communities, and classes players chose for quick reference

### For Campaign Documentation

- Maintain session-by-session structure (Session Zero → Session One → Session Two, etc.)
- Record outcomes of combat using the narrative spotlight framework (who had spotlight, key decisions, consequences)
- Note any house rules or mechanical modifications with justification

## Integration Points & Dependencies

- All character creation relies on official Daggerheart rulebooks (PDFs in `Rulebook Excerpts/`)
- Session notes depend on Character Questionnaire responses for player context
- Combat encounters should reference the Quick Reference for difficulty scaling and adversary abilities
- External dependency: Official Daggerheart Core Rulebook (5-20-2025 version included)

## Key Collaboration Pattern

**GM-Led Narrative First**: As an AI assisting, prioritize narrative and story impact over mechanical precision. The GM is the "biggest fan" of the players—help craft spotlight moments that serve each character's arc based on their questionnaire responses, even if it means bending mechanics.
