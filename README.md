# asdf-azure-cli

<div align="left">
  <a href="https://asdf-vm.com/">
    <img src="https://img.shields.io/badge/doc-asdf-blue"/>
  </a>
  <img src="https://github.com/boris-ning-usds/asdf-azure-cli/workflows/CI/badge.svg" />
  <img src="https://github.com/boris-ning-usds/asdf-azure-cli/workflows/Lint/badge.svg" />
  <a href="https://choosealicense.com/licenses/0bsd/">
    <img src="https://img.shields.io/badge/License-BSD_0--Clause-orange.svg"/>
  </a>
</div>
<br/>

Forked and modified from [itspngu](https://github.com/itspngu/asdf-azure-cli) as the project has been archived.

This repository is a [azure-cli](https://github.com/Azure/azure-cli) plugin for the [asdf version manager](https://asdf-vm.com). [asdf plugin](https://github.com/asdf-vm/asdf-plugins) is a convenient way to install a large number of command line tools of various versions and to upgrade with a [flat-file](https://asdf-vm.com/manage/configuration.html#tool-versions).

## Contents

- [Plugin Dependencies](#plugin-dependencies)
- [Install](#install)
- [License](#license)

## Plugin Dependencies

- `curl` - for azure-cli downloads from upstream releases
- `python3` (with `pip` and `venv` modules) - for installing and running the cli where [version 2.54.0 release supports python 3.11](https://github.com/MicrosoftDocs/azure-docs-cli/blob/main/docs-ref-conceptual/release-notes-azure-cli.md#packaging).

## Install

Plugin:

```bash
asdf plugin-add azure-cli https://github.com/boris-ning-usds/asdf-azure-cli
```

azure-cli:

```bash
# Show all installable versions
asdf list-all azure-cli

# Install specific version
asdf install azure-cli latest

# Set a version globally (in your ~/.tool-versions file)
asdf global azure-cli latest

# Run azure-cli
az --version
> azure-cli 2.54.0
[...]
```

Refer to the [upstream azure-cli repository](https://github.com/Azure/azure-cli) for documentation and usage instructions.

Check the [asdf](https://github.com/asdf-vm/asdf) readme for more instructions on how to install & manage versions.

## Uninstall

```bash
asdf plguin remove azure-cli
```

## License

See [LICENSE](LICENSE).
