TODO:  If I include a manual `dependabot.yml` file and thereby disable auto-submission, and if I include a mix of coding languages, all of which are eligible to be SBOM-scanned by GitHub's Dependabot and even normally would auto-submit, note that because of my manual override that forgot one of the languages, a language ends up failing to appear in the SBOM.

* https://docs.github.com/en/code-security/concepts/supply-chain-security/dependency-graph-data#dependabot-graph-jobs
* https://docs.github.com/en/code-security/reference/supply-chain-security/dependency-graph-supported-package-ecosystems#supported-package-ecosystems

I'm expecting GitHub Actions's `actions/checkout` in [this repo's SBOM](https://api.github.com/repos/kkgthb/gh-sbom-with-mixed-auto-submission/dependency-graph/sbom), but for NPM's `express` and `shx` to be missing even though NPM normally should auto-submit, because I forgot to mention NPM in the `dependabot.yml` file.