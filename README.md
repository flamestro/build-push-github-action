# build-push-github-action

To use this action you need to have a docker file in your repository.
This action will then publish your docker image for you in github packages (ghcr.io).

## Usage

``` yaml
- name: publish docker image
  uses: flamestro/build-push-github-action@v1.2.0
  with:
    token: ${{ secrets.PAT_WRITE_PACKAGES }}
```

you can also pass 
`username: your-ghcr-username` (defaults to the action actor)

Note: Instead of `PAT_WRITE_PACKAGES` you can also use GITHUB_TOKEN. However, your repo must allow the GITHUB_TOKEN to write packages.
