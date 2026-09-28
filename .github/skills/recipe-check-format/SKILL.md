# Recipe Check and Format Skill

## Purpose
Use this skill to validate and normalize markdown recipe files in this repository.

The repository’s recipes follow a consistent structure, and the formatter should preserve that pattern while fixing minor formatting drift.

## Canonical recipe structure
Each recipe file should follow this order:

1. Back link to the table of contents
2. H1 title
3. Optional source attribution line
4. One or more section headings in bold
5. Ingredient list(s)
6. Process steps

### Required layout
- The file begins with: `[назад в оглавление](../README.md)`
- The title is an H1: `# Recipe Name`
- Section headings are bold and use consistent wording:
  - `**Ингредиенты**` / `**Ingredients**`
  - `**Специи**` / `**Topping**`
  - `**Маринад**`
  - `**Процесс**` / `**Process**`
- Ingredient items use bullet lists (`-` preferred; `*` is acceptable if already used consistently)
- Process steps use ordered lists (`1.`, `2.`, etc.)
- Leave one blank line between sections
- Keep source attribution as its own paragraph before the ingredient list when a link is included

## Formatting rules
- Preserve the recipe title exactly as written, including original language and naming style
- Normalize heading capitalization and spacing
- Use consistent punctuation: sentence fragments in steps end with a period when appropriate
- Keep unit formatting consistent, for example: `1.5 ч.л.`, `500 гр.`, `450 мл.`, `2 кг.`
- Use consistent decimal style: `1.5` not `1,5` in English-style numeric formatting, unless the file is already written in a local style and should remain that way
- Maintain transliteration and original names if a recipe uses an English title or ingredient names
- Do not invent ingredients or steps; only fix textual structure and consistency

## Validation checklist
Before finalizing a file, verify:

- It has a title
- It includes a back-to-README link at the top
- It has at least one ingredient block
- It has a process section
- The headings are in the expected order
- Lists are not empty
- Formatting is visually consistent and readable
- There are no duplicate or missing section names
- If an external recipe source is cited, the link is preserved

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
