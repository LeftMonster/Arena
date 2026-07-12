# PROJECT_HANDOFF.md

# LoL Arena / ARAM Mayhem Mechanics Research

## Handoff for Codex Agent

Last Updated: 2026-07-13

------------------------------------------------------------------------

# 1. Project Goal

Build a long-term mechanics database for League of Legends ARAM: Mayhem
(Arena-style Augments).

This is **NOT** a build guide.

The goal is to reverse-engineer game mechanics.

Priority:

1.  Riot official sources
2.  Riot patch notes
3.  Riot developer blogs
4.  Community League Wiki / maintained databases
5.  Experiments
6.  Theory (must be labeled)

Never treat community assumptions as official facts.

------------------------------------------------------------------------

# 2. Current Research Principles

Always analyse in this order:

Ability Augment ↓

Champion mechanics

↓

Event Tree

↓

Normal Augments

↓

Items

↓

Interactions

↓

Experiments

Never start directly from build recommendations.

------------------------------------------------------------------------

# 3. Core Concepts Already Established

## Attack Count

Number of attacks.

## Hit Count

Number of successful hits.

## Apply Count

Number of Apply On-Hit executions.

Apply Count != Hit Count.

Many Arena mechanics (Mystic Punch etc.) care about Apply Count instead
of Attack Count.

------------------------------------------------------------------------

# 4. Event Types

Current known event categories:

-   Attack
-   Hit
-   Apply On-Hit
-   Spell Damage
-   Spellblade
-   Buff
-   Debuff
-   Cooldown Modifier
-   Cooldown Reset
-   Delayed Trigger
-   Revive

------------------------------------------------------------------------

# 5. Champion Classes

Current internal classification:

-   On-Hit Carry
-   On-Hit Caster
-   Spell Combo
-   Spell Utility
-   Spellblade Hero
-   Attack Modifier Hero

Examples:

Master Yi: On-Hit Carry

Gangplank: On-Hit Caster

Ryze: Spell Combo

Zilean: Spell Utility

Corki: Spellblade Hero

Ashe: Attack Modifier Hero

------------------------------------------------------------------------

# 6. Important Champion Conclusions

## Master Yi

Research focus:

-   Q Apply On-Hit
-   E True Damage
-   Mystic Punch
-   Ethereal Weapon
-   Dusk and Dawn

------------------------------------------------------------------------

## Gangplank

Research focus:

-   Barrel
-   Spellblade
-   On-Hit interactions

------------------------------------------------------------------------

## Ryze

Current strongest observed Ability Augment:

Other abilities reset E cooldown.

Current research:

E becomes engine.

Need to optimize Augment combinations.

------------------------------------------------------------------------

## Corki

Important:

Current passive specially supports Spellblade.

Do NOT classify Corki as generic On-Hit champion.

Research direction:

Spellblade interactions.

------------------------------------------------------------------------

# 7. Current Arena Topics

High priority:

Mystic Punch

Dusk and Dawn

Ethereal Weapon

Archmage

Back to Basics

Phenomenal Evil

Mind to Matter (official CN: 由心及物)

Jeweled Gauntlet

------------------------------------------------------------------------

# 8. Terminology Rules

Use official Chinese names whenever confirmed.

Store:

Official Chinese

English

Patch

Source

Mechanic Class

Research Status

------------------------------------------------------------------------

# 9. Documentation Rules

Every conclusion must be one of:

🟢 Confirmed by Riot

🟡 Verified by experiment

🔴 Theory only

Never mix these.

------------------------------------------------------------------------

# 10. Current Files

Skill

Glossary

Arena Augments Database

Roadmap

Hero Archive

Keep version history.

------------------------------------------------------------------------

# 11. Immediate Next Task

Continue building Arena Augment database.

Target:

Collect ALL current Augments (\~250+)

For every Augment:

-   Official CN
-   English
-   Tier
-   Full description
-   Patch history
-   Mechanic classification
-   Research notes
-   Source
-   Verification status

Do NOT skip entries.

This database is currently the highest priority task.
