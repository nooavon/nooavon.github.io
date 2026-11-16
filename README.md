# nooavon.github.io

Source for my portfolio website, **[nooavon.github.io](https://nooavon.github.io)**.

I'm an Economics and Business Analytics student at Aalto University, looking for a summer 2027 traineeship in economic analysis, data analytics or forecasting. The site collects my thesis, course projects and CV.

## What's on the site

- **[About](https://nooavon.github.io/)**: who I am and what I'm looking for
- **[CV](https://nooavon.github.io/cv/)**: education, projects, experience and skills, plus a [PDF version](https://nooavon.github.io/files/Nooa_von_Schoneman_CV.pdf)
- **[Projects](https://nooavon.github.io/projects/)**: my bachelor's thesis and course projects, each with code or a report

## Where things live

| Path | Contents |
|---|---|
| `_pages/` | About, CV and Projects pages |
| `_portfolio/` | One Markdown file per project (`order:` in the front matter sets its place on the Projects page) |
| `images/` | Figures used on project pages; `images/og/` holds link-preview images |
| `files/` | CV and other PDFs |
| `_config.yml` | Site settings, sidebar bio and contact links |

## Running locally

With Docker Desktop running:

```bash
docker compose up -d --build
docker compose exec jekyll-site bundle exec jekyll serve --host 0.0.0.0
```

Then open <http://localhost:4000>.

## Credits

Built with [Academic Pages](https://github.com/academicpages/academicpages.github.io), a fork of the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) Jekyll theme. The theme code is under the MIT license in [LICENSE](LICENSE).
