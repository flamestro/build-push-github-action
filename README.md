# build-push-github-action

To use this action you need to have a docker file in your repository.
This action will then publish your docker image for you in github packages (ghcr.io).

## Usage

``` yaml
- name: publish docker image
  uses: flamestro/build-push-github-action@v1.2.0
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```
To use the GITHUB_TOKEN you need to enable write access for it in your repo -> settings -> actions -> general -> read and write access
