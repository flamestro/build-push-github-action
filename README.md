# build-push-github-action

To use this action you need to have a docker file in your repository.
This action will then publish your docker image for you in github packages (ghcr.io).

## Usage

``` yaml
- name: publish docker image
  uses: flamestro/build-push-github-action@v1.9.0
  with:
    username: ${{ github.repository_owner }}
    token: ${{ secrets.GITHUB_TOKEN }}
    # Optional: publish multi-arch image manifests
    platforms: linux/amd64,linux/arm64
    # Optional: enable Buildx GHA cache
    cache: true
    cache_scope: my-image-${{ matrix.arch }}
```

## Inputs

- `cache` (optional): Enable Buildx GitHub Actions cache (`true` / `false`), default `false`.
- `cache_scope` (optional): Cache scope key used when cache is enabled, default `build-push-github-action`.
- `cache_mode` (optional): Cache export mode (`min` or `max`), default `max`.

!!! ATTENTION !!! To use the GITHUB_TOKEN you need to enable write access for it in your repo -> settings -> actions -> general -> read and write access
