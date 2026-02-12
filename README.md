# Interface Design

<p align="center">
  <strong>Craft · Consistency</strong>
</p>

<p align="center">
  A Claude Code skill for building interfaces with intention.
</p>

<p align="center">
  <em>For dashboards, apps, tools, admin panels. Not for marketing sites.</em>
</p>

---

## What This Does

When Claude builds UI, it defaults to the average of its training data — the same card layouts, the same spacing, the same shadows everyone else gets. Interface Design replaces that with a principle-based design process that produces interfaces tied to the specific product being built.

The skill teaches Claude to:

- **Explore the product's domain** before writing code — understanding the world the product lives in, the colors that belong there, and what makes it distinct
- **Make intentional design decisions** — spacing, depth, surfaces, typography — with reasoning behind each choice
- **Self-critique after building** — evaluating composition, craft, content coherence, and code structure, then fixing what defaulted

## Installation

### Plugin

```bash
/plugin marketplace add peterlowrance/interface-design-stateless
/plugin menu
```

Select `interface-design` from the menu. Restart Claude Code.

### Manual

```bash
git clone https://github.com/peterlowrance/interface-design-stateless.git
cp -r interface-design-stateless/.claude/* ~/.claude/
cp -r interface-design-stateless/.claude-plugin/* ~/.claude-plugin/
```

Restart Claude Code.

---

## How It Works

The skill activates when you ask Claude to build interface design. It follows a five-step flow:

1. **Explore** — Maps the product's domain, color world, signature element, and default rejections
2. **Propose** — Suggests a direction grounded in that exploration
3. **Confirm** — Gets your buy-in before building
4. **Build** — Applies design principles: token architecture, spacing systems, depth strategy, typography hierarchy, interaction states
5. **Critique** — Evaluates the build for composition, craft, content, and structure — then rebuilds what fell back to defaults

Every design choice must be explainable. If the answer is "it's common" or "it works," the skill treats that as a default, not a decision.

---

## What's Inside

```
.claude/skills/interface-design/
  SKILL.md                ← Core skill: philosophy, principles, workflow, evaluation
  references/
    principles.md         ← Technical details, token architecture, code examples
    example.md            ← Practical examples of subtle layering decisions
```

**SKILL.md** covers the full design process — from understanding where defaults hide, through domain exploration and craft foundations, to the post-build critique protocol.

**references/principles.md** has the specifics: surface elevation scales, text hierarchy tokens, border progression, spacing systems, depth strategies, dark mode considerations, and code examples.

**references/example.md** walks through real decisions — how to handle a sidebar dropdown's surface, how to choose an input's focus state, how stacked surfaces should relate.

---

## The Test

> If another AI given a similar prompt would produce the same output, the skill has failed. The interface must emerge from this user, this problem, this intent.

---

## License

MIT — See [LICENSE](LICENSE)
