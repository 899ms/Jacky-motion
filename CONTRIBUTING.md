# Contributing

This repository is primarily maintained for Jacky's content workflow and distributed as one unified Skill with two output modes:

- `standard`: script to manually controlled HTML, in 16:9 or 3:4.
- `srt`: script plus corrected SRT to timed autoplay HTML with B-roll recording frames, in 16:9.

Useful contributions should keep the core constraints intact:

- Improve information clarity before visual decoration.
- Keep generated output browser-openable and recording-friendly.
- Avoid adding heavy rendering dependencies to the default path.
- Keep each visual style internally consistent.
- Keep the runtime cores in `assets/base-template.html`, `assets/base-template-portrait.html`, and `assets/base-template-srt.html` unchanged unless the runtime itself is the subject of the change.
- Preserve final-state-first animation behavior and the registered beat/layout attributes.
- Run the matching validator against a representative output before submitting:

```bash
node scripts/validate-motion-html.mjs path/to/standard-output.html
node scripts/validate-motion-html-srt.mjs path/to/srt-output.html
```

Browser layout checks are optional. When Playwright is unavailable, use an agent browser or manual screenshot review instead.

For style changes, update both `styles/` and `assets/styles/`.
