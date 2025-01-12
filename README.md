# static-websites

This repository stores and generates static files for previous and current EuroPython websites.

## How are the static files generated?
**2022+:** The static files are generated with GitHub action workflows using the source code from the [EuroPython website repository](https://github.com/EuroPython/website) and its branches.
**Older years:** The static files are either scraped or manually generated.

## Structure of this repository
- `main` branch: Contains this README file and the workflow files.
- `<year>` branches: Contains the static files for the respective year.

## How it works
1. The dispatcher workflow in the `main` branch triggers the respective <year> workflow when a new commit is pushed to the <year> branch of the [website repository](https://github.com/EuroPython/website).
2. The <year> workflow generates the static files and pushes them to the respective <year> branch of this repository.
3. The static files are then deployed to our static server.
4. The website is live!