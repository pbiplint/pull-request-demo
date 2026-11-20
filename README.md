# pbiplint pull request demo

The Messy Sales Demo from [pbiplint](https://pbiplint.com), with its 19 errors fixed, and a workflow that lints every pull request.

- `Messy Sales Demo.pbip` is the Power BI project: the sample that ships with pbiplint (`npx pbiplint --sample`), with fictional data.
- `.github/workflows/pbiplint.yml` runs [pbiplint/action](https://github.com/pbiplint/action) on every pull request and every push to `main`. A branch rule requires that check, so nothing merges into `main` while it's red.
- The warnings and info findings are still here on purpose, because the default gate fails only on errors.
- The CSV sources point at `C:\Demo\Sales\Data\` on the machine I recorded with. The CSVs aren't in this repository, and pbiplint doesn't need them.

I built this for a video on [The Data Practitioner](https://www.youtube.com/@TheDataPractitioner).

This repository is public, so its runs and code scanning alerts are too. Before you add pbiplint to a public repository of your own, know that the findings name your tables, columns, measures, and queries.
