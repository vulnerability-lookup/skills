# Vulnerability-Lookup skills

Agent skills that use [Vulnerability-Lookup](https://vulnerability.circl.lu), in the
Agent Skills format (`SKILL.md`), which Claude Code and other coding agents can load.

| Skill | What it does |
| --- | --- |
| [vulnerability-lookup](skills/vulnerability-lookup/SKILL.md) | Triage a vulnerability or a dependency alert: CVSS, EPSS, KEV catalogues, sightings, VEX, linked advisories and fixed versions, then a patch priority |

## Install

Copy a skill directory where your agent looks for skills, for example for Claude Code:

```bash
cp -r skills/vulnerability-lookup ~/.claude/skills/        # for you
cp -r skills/vulnerability-lookup .claude/skills/          # for one project
```

The helper script needs Python 3.8 or later and nothing else. It queries the public
instance by default; set `VULNERABILITY_LOOKUP_URL` to use your own.

## Acknowledgements

The triage report follows the fields that ENISA's
[secure-package-consumption](https://github.com/enisaeu/agentic-skills) skill asks for
a vulnerability alert (severity, EPSS, KEV, reachability, VEX status, remediation).
