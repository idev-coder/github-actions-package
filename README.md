# Get node package info 

Action for getting information from package.json file

## Inputs

### `path`

Path to package.json file. `./` by default.

## Outputs

### `name`

Package name

### `version`

Package version


Is the package version a release candidate

Available since v1.0

## Example usage

```
- name: Github Actions Package
  id: package
  uses: idev-coder/github-actions-package@v1.0

- name: Get the output
  run: |
    echo "name: ${{ steps.package.outputs.name }}"
    echo "version: ${{ steps.package.outputs.version }}"
    echo "description: ${{ steps.package.outputs.description }}"
    echo "main: ${{ steps.package.outputs.main }}"
    echo "scripts: ${{ steps.package.outputs.scripts }}"
    echo "keywords: ${{ steps.package.outputs.keywords }}"
    echo "author: ${{ steps.package.outputs.author }}"
    echo "license: ${{ steps.package.outputs.license }}"
```