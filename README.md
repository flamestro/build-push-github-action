# build-push-github-action

To use this action you need to have a docker file in your repository.
This action will then publish your docker image for you in github packages (ghcr.io).

## Usage

``` yaml
- name: publish docker image
  uses: flamestro/build-push-github-action@v1.7.4
  with:
    username: ${{ github.repository_owner }}
    token: ${{ secrets.GITHUB_TOKEN }}
```
!!! ATTENTION !!! To use the GITHUB_TOKEN you need to enable write access for it in your repo -> settings -> actions -> general -> read and write access
