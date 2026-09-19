# CLAUDE.md

A static GitHub Pages site (`index.html` + `styles.css`) that ranks strange biology topics as an "iceberg meme," with topics getting stranger the deeper the section.

## Your job in this repo

At this point, the only task is **adding entries to the iceberg**. The user gives you three things:

1. A link
2. A title — the text shown on the iceberg
3. Which iceberg section it belongs in

You add it to `index.html`, matching the existing entries.

## How to add an entry

Sections live in `index.html` as `div.iceberg_section` blocks, in order from shallowest to deepest:

| Class | Heading |
| --- | --- |
| `s1` | Tip of the Iceberg |
| `s2` | The Shallows |
| `s3` | The Midpoint |
| `s4` | Sinking Deeper |
| `s5` | Into the Depths |

The user may name the section either way (by heading or by `s1`–`s5`); both refer to the same block.

Append a new `<li>` at the **end** of that section's `<ul>`, on its own line, indented to match its neighbors (20 spaces):

```html
<li><a href="LINK">Title</a></li>
```

Conventions to follow:

- Wrap scientific names (genus/species, e.g. `<i>Turritopsis dohrnii</i>`) in `<i>` inside the `<a>`.
- Some entries are a quotation from the linked source rather than a topic name; keep the user's title verbatim, including quotes and any `[...]` bracketing.
- Don't reorder or re-rank existing entries, and don't edit `styles.css` — placement is the user's call, made by vibes (see `README.md`).
- One entry per commit, message in the form `Add vulture bees`.
