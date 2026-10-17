# AGENTS.md

A collection of cooking recipes in Markdown, mostly in Russian. Recipes live in `salads/`, `soups/`,
`main_dishes/`, `bakery/`, and `drinks/`; `README.md` is the table of contents.

## Adding a recipe

- Put the file in the matching category directory with a lowercase snake_case name, e.g.
  `main_dishes/chicken_curry.md`. Images go next to it.
- Add a link to `README.md` under the matching `##` section, in the same `[Title](dir/file.md)`
  form, separated from its neighbours by a blank line.

## Recipe layout

The layout is a loose convention, not a schema. A recipe has, in order:

1. `[назад в оглавление](../README.md)` on the first line.
2. An H1 title.
3. Optionally, a source link or a short intro paragraph.
4. One or more bold section labels, each followed by a list: ingredients, components, or stages.
   Common labels are `**Ингредиенты**`, `**Специи**`, `**Маринад**`, `**Соус**`, `**Процесс**`, and
   in English recipes `**Ingredients**` and `**Process**`. Recipe-specific stages such as
   `**Опара**`, `**Тесто**`, or `**Закваска**` are fine when they describe a real step.
5. A process section, as a numbered or bulleted list.

## Editing rules

- Do not invent or change ingredients, quantities, steps, or source links.
- Keep the title, the recipe's language, and its transliterations as written.
- Within one file, keep one bullet style (`-` or `*`), one list indentation, and one unit style
  (`500 гр.`, `1.5 ч.л.`, `450 мл.`, `2 кг.`). Do not change another file's style to match.
- Collapse runs of blank lines and trim trailing whitespace.
- Prefer the smallest cleanup that fixes the problem. Do not force an unusual but valid layout into
  the template above.

## Checking a recipe

Before finishing, confirm the file has the back link, a title, a non-empty ingredient or component
list, and process instructions; that every section label matches its content and none is
duplicated; and that the recipe is linked from `README.md`.
