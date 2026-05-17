# 🐼 Panda Theme – Style Test

This file showcases every style applied by the **Panda Syntax** Obsidian theme — headings, text, links, callouts, code, tables, and more. Use it in Obsidian with the theme installed to see the full effect.

---

## Headings

# H1 — Heading One (cyan)
## H2 — Heading Two (pink)
### H3 — Heading Three (orange)
#### H4 — Heading Four (blue)
##### H5 — Heading Five (purple)
###### H6 — Heading Six (foreground)

---

## Text Styles

Normal body text should be soft white in dark mode, near-black in light mode.

**Bold text** renders in pink — use for emphasis.
*Italic text* renders in orange — use for nuance.
***Bold italic*** combines both treatments.
~~Strikethrough~~ for deprecated or removed content.

Inline `code` renders in teal on a subtle dark background.

==Highlighted text== uses a warm yellow-orange wash.

---

## Links

- Internal wikilink: [[Panda Theme – Style Test]]
- Unresolved link: [[A Note That Does Not Exist]]
- External link: [Panda Syntax on GitHub](https://github.com/PandaTheme/panda-syntax-vscode)

---

## Tags

#panda #theme #obsidian #style-test

---

## Lists

### Unordered
- Item one
- Item two
  - Nested item A
  - Nested item B
- Item three

### Ordered
1. First step
2. Second step
3. Third step

### Task List
- [ ] Incomplete task
- [x] Completed task
- [ ] Another open item

---

## Blockquote

> "The best themes are invisible — they get out of the way and let the content breathe."
>
> — Nobody, probably

---

## Tables

| Token type   | Color     | Example                  |
|--------------|-----------|--------------------------|
| Keyword      | Pink      | `const`, `return`, `if`  |
| String       | Cyan      | `"hello world"`          |
| Number       | Orange    | `42`, `3.14`             |
| Function     | Blue      | `readFileSync()`         |
| Comment      | Muted     | `// this is a comment`   |
| Operator     | Pink      | `===`, `=>`, `+`         |

---

## Callouts

> [!NOTE]
> A **note** callout. Use for supplementary context.

> [!INFO]
> An **info** callout. Neutral, informational tone.

> [!TIP]
> A **tip** callout. Use for helpful shortcuts or suggestions.

> [!SUCCESS]
> A **success** callout. Task complete, all good.

> [!IMPORTANT]
> An **important** callout. Pink — don't skip this.

> [!QUESTION]
> A **question** callout. Use for open questions or FAQs.

> [!WARNING]
> A **warning** callout. Something might go wrong.

> [!DANGER]
> A **danger** callout. Destructive action or critical error.

> [!BUG]
> A **bug** callout. Something is broken.

> [!TODO]
> A **todo** callout. Action item that needs a follow-up.

> [!EXAMPLE]
> An **example** callout. Purple — illustrative content.

> [!QUOTE]
> A **quote** callout. Muted — for citations and attributions.

> [!ABSTRACT]
> An **abstract** callout. Summary or TLDR content.

---

## Code — TypeScript

```ts
interface Theme {
  name: string;
  version: string;
  author: string;
}

// Load and bump the manifest version
function bumpVersion(manifest: Theme, next: string): Theme {
  const updated = { ...manifest, version: next };
  console.log(`Bumped to ${next}`);
  return updated;
}

const panda: Theme = {
  name: "Panda Syntax",
  version: "1.0.0",
  author: "Yanna Lin",
};

export default bumpVersion(panda, "1.1.0");
```

## Code — Python

```python
from dataclasses import dataclass
from typing import Optional

@dataclass
class Token:
    kind: str       # keyword, string, number, comment…
    value: str
    line: int
    col: Optional[int] = None

def tokenize(source: str) -> list[Token]:
    """Split source code into tokens."""
    tokens: list[Token] = []
    for i, line in enumerate(source.splitlines(), start=1):
        if line.strip().startswith("#"):
            tokens.append(Token("comment", line, i))
        elif line.strip().startswith("def ") or line.strip().startswith("class "):
            tokens.append(Token("keyword", line.split()[0], i))
    return tokens

# Example
src = """
def hello():
    return "world"  # 42
"""
print(tokenize(src))
```

## Code — CSS

```css
:root {
  --panda-pink: #FF90D0;
  --panda-cyan: #45A9F9;
  --panda-green: #19F9D8;
}

.theme-dark {
  --background-primary: #1f1f1f;
  --text-normal: #E6E6E6;
  --bold-color: var(--panda-pink);     /* pink */
  --italic-color: var(--panda-orange); /* orange */
}

/* File explorer hover */
.nav-file-title:hover {
  background-color: color-mix(in srgb, var(--panda-pink) 15%, transparent);
}
```

## Code — Shell

```bash
# Clone the theme and install
git clone https://github.com/linyanna/panda-syntax-obsidian
cd panda-syntax-obsidian

# Copy to vault
cp -r . ~/.obsidian/themes/Panda\ Syntax/

echo "Theme installed successfully 🐼"
```

---

## Frontmatter Preview

The frontmatter block at the top of this file (`tags`, `created`) should appear with muted text and a subtle background.

---

## Scrollbar

Scroll this note to see the custom thin scrollbar — 6 px wide, styled in the border color, turning muted on hover.
