# IRENE-AE9/AP9/SPM Website (GitHub Pages)

This repository hosts the public website for the IRENE-AE9/AP9/SPM radiation belt and space plasma specification models, developed by the Air Force Research Laboratory (AFRL).

**Live site:** https://yourusername.github.io/ae9ap9/

## Distribution Statement

Distribution Statement A: Approved for public release; distribution unlimited.

## Site Structure

```
/                        → Home (index.md)
/_layouts/default.html   → Shared page layout
/assets/css/style.css    → Stylesheet
/assets/docs/            → PDFs (release notes, user guides, presentations)
/assets/images/          → Images
/pages/
  news.md
  factsheet.md
  downloads.md
  documents.md
  team.md
  validations.md
  dsx.md
  register.md
  quick-reference/
    index.md
    energy.md
    architecture.md
    datasets.md
    modes.md
    time-sampling.md
    issues-and-limits.md
    versions-public.md
    future.md
    best-practices.md
  documents/
    tech-docs.md
    technical-documentation-report.md
  validations/
    independent.md
  dsx/
    publications.md
```

## Updating Content

1. Obtain OPSEC release for new content
2. Edit the relevant `.md` file
3. Commit and push — GitHub Pages rebuilds automatically (usually < 1 min)

## Adding PDFs and Documents

Place PDFs in `assets/docs/` and link them from the appropriate Markdown page:

```markdown
[User's Guide](../assets/docs/IRENE_Users_Guide.pdf)
```

## Large File Downloads (Model Package)

The model package (240-600 MB) **cannot** be hosted directly in this repo (GitHub 100 MB file limit). Options:
- Host on Google Drive / OneDrive and link from `pages/downloads.md`
- Use a pre-signed URL from cloud storage (S3, GCS, Azure Blob)
- Link to a Releases asset (GitHub Releases supports up to 2 GB per file via LFS)

## Setup

This site uses Jekyll with a custom layout (no theme dependency).

To run locally:
```bash
bundle exec jekyll serve
```

Gemfile:
```ruby
gem "jekyll", "~> 4.3"
gem "jekyll-relative-links"
```

## Contact

[AFRL.RVBXR.AE9.AP9.Org.Mbx@us.af.mil](mailto:AFRL.RVBXR.AE9.AP9.Org.Mbx@us.af.mil)
