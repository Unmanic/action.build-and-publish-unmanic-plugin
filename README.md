# action-build-and-publish-unmanic-plugin
A GitHub action that automatically builds and publishes a release of a Unmanic Plugin to to its GitHub repository.

## Inputs

### `python_version` 

**Optional** - Python version for building [Default `3.11`].

### `node_version` 

**Optional** - Node version for building [Default `20`].

### `github_token` 

**Optional** - A personal access token (PAT) used to fetch tag and publish the release [Default: `${{ github.token }}`].

## Example usages

Specifically use an older version of NodeJS for building the plugin:
```yaml
- name: Build and publish plugin
  uses: Josh5/action-build-and-publish-unmanic-plugin@master
  with:
    node_version: 16
```

Specify a custom GitHub PAT
```yaml
- name: Build and publish plugin
  uses: Josh5/action-build-and-publish-unmanic-plugin@master
  with:
    github_token: ${{ secrets.GH_TOKEN }}
```
