# SuperCollider Flatpak

* [SuperCollider](https://supercollider.github.io/)
* [Flatpak](https://www.flatpak.org/)

## Build

Install dependencies:

```sh
flatpak install org.kde.Sdk//5.15-22.08
```

Build the package
```sh
 flatpak-builder --ccache --repo=flatpak_repo --force-clean build-dir io.github.supercollider.SuperCollider.yml
```

Build the bundle
```sh
 flatpak build-bundle flatpak_repo SuperCollider.flatpak io.github.SuperCollider
```

## Install bundle locally

```sh
flatpak install --user SuperCollider.flatpak
```

## Run

scide (default):

```sh
flatpak run io.github.SuperCollider
```

sclang:
```sh
flatpak run --command=sclang io.github.SuperCollider path/to/file.sc
```
