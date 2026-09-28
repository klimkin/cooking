# Recipe Check and Format Skill

## Purpose
Use this skill to validate and normalize markdown recipe files in this repository.

The repository’s recipes follow a consistent structure, and the formatter should preserve that pattern while fixing minor formatting drift.

## Canonical recipe structure
This repository uses a loose but recognizable recipe template rather than one single rigid schema.

The common structure is:

1. Back link to the table of contents
2. H1 title
3. Optional source attribution or intro paragraph
4. One or more bold section headings describing ingredients, prep, sauces, or stages
5. Ingredient or component lists
6. A process description or step list

### Typical repo patterns
- The file usually begins with: `[назад в оглавление](../README.md)`
- The title is usually an H1: `# Recipe Name`
- Common section labels include `**Ингредиенты**`, `**Ingredients**`, `**Специи**`, `**Маринад**`, `**Соус**`, `**Процесс**`, and `**Process**`
- Valid recipe-specific labels also appear, such as `**Опара**`, `**Тесто**`, `**Закваска**`, or `**Вывод ржаной закваски**`
- Ingredient lists are usually bullets, but the repo accepts both `-` and `*` styles when they are already used consistently in the file
- Process sections may use numbered steps or a bullet list, depending on the recipe author
- Extra sections are acceptable when they describe a real recipe stage or preparation step
- Source attribution should stay adjacent to the recipe introduction when present

## Formatting rules
- Preserve the recipe title exactly as written, including original language and naming style
- Keep the heading structure readable and semantically meaningful rather than forcing a single universal heading set
- Normalize spacing and markdown list formatting without changing the recipe’s meaning
- Use consistent punctuation: sentence fragments in steps should end with a period when appropriate
- Keep unit formatting consistent within a recipe, for example: `1.5 ч.л.`, `500 гр.`, `450 мл.`, `2 кг.`
- Maintain original transliteration and recipe names if a file is written partly in English or Russian
- Do not invent ingredients, steps, measurements, or source links
- Prefer minimal, repository-consistent cleanups over broad rewriting

## Validation checklist
Before finalizing a file, verify:

- It has a title
- It includes a back-to-README link at the top
- It includes a clear ingredient or component section
- It includes a process section or equivalent cooking instructions
- The structure is readable and ordered logically
- The headings are consistent with the recipe’s actual content
- Lists are not empty and formatting is visually coherent
- Any extra sections are real recipe stages, not accidental duplicates
- If an external recipe source is cited, the link is preserved
- The edit does not over-normalize valid but unusual recipe layouts

## Normalization behavior
When formatting a recipe, the tool should:

- collapse extra blank lines
- trim trailing whitespace
- keep a recipe’s original meaning and structure intact
- standardize markdown formatting without stripping useful recipe-specific sections
- prefer lightweight cleanup over rigid template enforcement

## Normalization behavior
When formatting a recipe, the tool should:

- collapse extra blank lines
- trim trailing whitespace
- ensure list indentation is consistent
- keep the same content while improving readability
- preserve original recipe intent and wording whenever possible

## Examples of compliant recipes
This repo contains the expected patterns, including:

- Russian recipes with sections like `**Ингредиенты**` and `**Процесс**`
- English recipes with `**Ingredients**` and `**Process**`
- Mixed-language recipes, including transliterated ingredients and local names
- Source links above the ingredient list, such as the Borscht recipe

## Output expectation
The formatted recipe should remain minimal, readable, and repository-consistent. The main goal is not rewriting the recipe, but checking that it matches the repository’s established recipe template and standard markdown formatting.
