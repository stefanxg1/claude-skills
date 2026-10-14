# claude-skills

Stefan's personal Claude skills. Every Claude Code cloud session copies them into `~/.claude/skills`, so they're available in any project.

## How it loads
The cloud environment's **Setup script** runs this at the start of each session:

```sh
git clone -q --depth 1 https://github.com/stefanxg1/claude-skills /tmp/claude-skills && mkdir -p ~/.claude/skills && cp -r /tmp/claude-skills/skills/* ~/.claude/skills/ || true
```

## Add a skill
Put its folder (with a `SKILL.md`) under `skills/`. New sessions pick it up.

## What's here
### Taste pack
From [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) (MIT). All are for **web** work, except `imagegen-frontend-mobile` (app screen concepts as images) and `output-skill`.

| Folder | Skill name | Use it for |
| --- | --- | --- |
| taste-skill | design-taste-frontend | Art direction for landing pages and sites, with a browser inspector (needs Node 22 + Chrome) |
| redesign-skill | redesign-existing-projects | Audit and upgrade an existing site |
| minimalist-skill | minimalist-ui | Clean, editorial, Notion/Linear-style UI |
| soft-skill | high-end-visual-design | Soft, premium look |
| brutalist-skill | industrial-brutalist-ui | Swiss type, raw mechanical layouts (beta) |
| gpt-tasteskill | gpt-taste | Awwwards-style pages with GSAP motion |
| image-to-code-skill | image-to-code | Generate a reference image, then build it |
| imagegen-frontend-web | imagegen-frontend-web | Website concept images only |
| imagegen-frontend-mobile | imagegen-frontend-mobile | Mobile app screen concept images only |
| brandkit | brandkit | Brand-kit overview images |
| stitch-skill | stitch-design-taste | Google Stitch-compatible design rules |
| output-skill | full-output-enforcement | Stops truncated code and placeholder comments |

### Design and UI
| Folder | Source | Use it for |
| --- | --- | --- |
| impeccable | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | Design, critique, audit and polish any interface, web or app. Downloads its own checksum-verified engine from the project's GitHub releases on first run |
| ui-ux-pro-max | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Searchable UI/UX knowledge base (styles, palettes, fonts, patterns) for web, mobile and desktop. Needs Python 3 |
| design-system | same | Token architecture and component specs |
| ui-styling | same | shadcn/ui + Tailwind interfaces |
| brand | same | Brand voice and identity guidelines |
| banner-design | same | Social, ad and hero banners |
| slides | same | HTML presentations |
| design | same | Logos, CIP, icons. AI image parts need a `GEMINI_API_KEY`, `ATLASCLOUD_API_KEY` or `MUAPI_API_KEY` |

### Motion
| Folder | Source | Use it for |
| --- | --- | --- |
| design-motion-principles | [kylezantos/design-motion-principles](https://github.com/kylezantos/design-motion-principles) | Purposeful motion, and audits that catch sloppy animation |
| gsap-core, gsap-timeline, gsap-scrolltrigger, gsap-plugins, gsap-react, gsap-frameworks, gsap-performance, gsap-utils | [greensock/gsap-skills](https://github.com/greensock/gsap-skills) | Official GSAP skills |

Each source's licence is at the repo root as `LICENSE-<source>`.

Left out on purpose: `taste-skill-v1` and `taste-skill-v2-experimental` (old versions of taste-skill that would compete with it).
