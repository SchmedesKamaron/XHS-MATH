# Math Markdown Style Guide for GitHub

This document defines the formatting rules for Markdown files containing mathematical formulas, designed for GitHub's built-in MathJax renderer.

Two styles are distinguished:
1. **Custom strict style**: used for homework / proof files (the one we used for the well-definedness problem).
2. **General loose style**: for ordinary notes and documentation.

> All spaces referred to in this guide are **ASCII half-width spaces**. Full-width Chinese spaces are forbidden around formulas.

## 1. Inline math: `$ ... $`

### Custom strict style (your requirement)
- There are **exactly two spaces** on both sides of the inline formula.
- The `$` symbols stick tightly to the math content; no spaces inside the dollar signs.
- If the formula is adjacent to punctuation marks, keep **two spaces** between the closing `$` and the punctuation.

✅ Correct:
```markdown
Let  $\sim$  be an equivalence relation on the set  $X$ .
For all  $x,y$  , we have  $x \sim y$  .
The proof is complete.  $\square$
```

❌ Wrong:
```markdown
Let $\sim$ be an equivalence relation.
Let  $ \sim $  be an equivalence relation.
For all $x,y$, we have $x\sim y$.
```

### General loose style (default for most repos)
- No mandatory surrounding spaces; write `Let $\sim$ be an equivalence relation.`
- Keep this for documentation, README, casual notes.

### Additional inline rules
- Do not put long multi-line equations inside inline `$ ... $`. Use display math instead.
- Never nest dollar delimiters: avoid `$a + $b$ + c$`.
- Prefer `\colon` for function mappings: `f \colon X \to Y`, not `f : X \to Y`.
- Use `$\square$` for end-of-proof marker. Under the strict style: `complete.  $\square$`.

## 2. Display math: `$$ ... $$`

These are centered, separate equations. Rules apply to both styles.

- Leave **one blank line above and one blank line below** the `$$` block.
- Opening `$$` and closing `$$` should each occupy their own line.
- Inside the block, use `\\` for line breaks. For aligned equations, use `\begin{aligned} ... \end{aligned}`.
- Punctuation belongs in the surrounding prose, not inside the display block unless mathematically necessary.

✅ Correct:
```markdown
The quotient set is defined as

$$
X / {\sim} = \{ [z] \mid z \in X \}
$$

where  $[z]$  denotes the equivalence class.
```

✅ Aligned example:
```markdown
We compute the difference

$$
\begin{aligned}
x' - y'
&= (x + k) - (y + m) \\
&= (x - y) + (k - m).
\end{aligned}
$$

Since  $k,m \in \mathbb Z$  , we have  $k - m \in \mathbb Z$ .
```

❌ Wrong:
```markdown
We have $$X/{\sim} = \{[z]\}$$ which is the quotient.
```

## 3. Global Markdown conventions

- File extension: `.md`.
- Filenames: lowercase, words separated by hyphens, e.g. `well-defined-proof.md`.
- Heading hierarchy: use `#`, `##`, `###` sequentially; do not skip levels.
- Use `---` as section separator, with blank lines before and after.
- Paragraphs are separated by a single blank line.
- Lists: prefer `-` for unordered lists, `1.` for ordered lists. Inline math inside lists still follows the selected style.
- HTML comments `<!-- comment -->` may be used for notes that should not render on GitHub.
- Keep source lines reasonably short for diff readability.

## 4. GitHub MathJax limitations & forbidden syntax

GitHub's native formula renderer only supports a subset of standard LaTeX.

✅ Supported
- `$ ... $` inline math
- `$$ ... $$` display math
- `\mathbb{R}, \mathbb{Z}, \mathbb{N}`
- `\sim, \star, \colon, \implies, \iff`
- `\begin{aligned} ... \end{aligned}`

❌ Avoid or do not use
- `\( ... \)` and `\[ ... \]` (unreliable on GitHub)
- `\newcommand`, `\def`, global macro definitions
- External `\usepackage` declarations
- Complex tikz, pgfplots, or ams packages beyond basic `amsmath`
- Chinese / full-width symbols inside formula bodies
- Mixing `$` and `$$` on the same source line

## 5. Quick reference template (strict style)

```markdown

## Theorem

Let  $X$  be a set and  $\sim$  an equivalence relation on  $X$ .
Define  $\star$  by

$$
[x] \star [y] = [f(x,y)].
$$

If  $x \sim x'$  and  $y \sim y'$  , then  $f(x,y) \sim f(x',y')$ .
Hence the operation is well-defined.  $\square$
```

## 6. When to use which style

- Use **custom strict style**: homework, typed proof solutions, problem sets, where consistent source formatting matters.
- Use **general loose style**: README, overview documents, notes for quick browsing, API descriptions.
- Do not mix styles within a single file. Pick one and follow it throughout the document.
