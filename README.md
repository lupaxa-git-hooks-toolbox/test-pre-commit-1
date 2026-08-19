<p align="center">
    <a href="https://github.com/lupaxa-git-hooks-toolbox">
        <img src="https://raw.githubusercontent.com/the-lupaxa-project/brand-assets/master/logos/organisations/git-hooks-toolbox/readme-logo.png" alt="Organisation Logo" />
    </a>
</p>

<h1 align="center">Test Pre-Commit 1</h1>

Validation pre-commit source for
[`setup-hooks`](https://github.com/lupaxa-git-hooks-toolbox/setup-git-hooks).
Use this repo to try the installer without a production hook. The script at
`src/pre-commit` only prints `hello`.

Examples pin this source with `version: HEAD` (current default branch).

## Validate setup-hooks

In a git working tree, add the YAML below, then run the CLI.

```yaml
# hooks/pre-commit-config.yml
- name: Hello one
  filename: hello-one
  url: https://github.com/lupaxa-git-hooks-toolbox/test-pre-commit-1
  version: HEAD
```

```yaml
# hooks/multiplexer-config.yml
url: https://github.com/lupaxa-git-hooks-toolbox/git-hooks-multiplexer
version: HEAD
```

```bash
python -m pip install lupaxa-setup-git-hooks
setup-hooks
```

That writes `hooks/pre-commit/01-hello-one` and installs the multiplexer.
A later `git commit` prints `hello`. Guide:
[Setup Git Hooks](https://setup-git-hooks.thelupaxaproject.org/).

<a href="https://github.com/the-lupaxa-project">
  <img src="https://raw.githubusercontent.com/the-lupaxa-project/brand-assets/master/logos/components/footer-for-child-orgs.svg" alt="The Lupaxa Project Footer" width="100%" />
</a>
