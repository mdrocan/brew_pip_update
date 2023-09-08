# Maintaining local environment with Ansible
Will be as an alternative for the maintenance bash scripts found in the shell-scripts repo: <https://github.com/mdrocan/shell-scripts>

## Script execution
- Execute with: `ansible-playbook update_brew.yml`

## Possible issues
- In some cases you may see the following error in the output:
`
fatal: [localhost]: FAILED! => {"changed": false, "msg": "Warning: These files were overwritten during the `brew link` step:\nError: The `brew link` step did not complete successfully"}
`

- This means that you should check with `brew doctor` which kegs are not properly linked and link them.

## Requirements
- Homebrew must already be installed on the target system

## Next steps
- Create same functionality for local testing and with Github Actions
### About
- Linter verified software

[![MegaLinter](https://github.com/mdrocan/brew_pip_update/workflows/MegaLinter/badge.svg?branch=main)](https://github.com/mdrocan/brew_pip_update/actions?query=workflow%3AMegaLinter+branch%3Amain)
