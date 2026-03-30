# Flatpak manifest for [Rclone Shuttle](https://github.com/pieterdd/RcloneShuttle)

### Build instructions
- In case of Rust dependency changes, get [flatpak-cargo-generator](https://pypi.org/project/flatpak-cargo-generator/) (not included here because license is unknown), install dependencies, then execute `flatpak-cargo-generator.py /path/to/code/repo/Cargo.lock -o /path/to/manifest/repo/cargo-sources.json`.
- In case of Go dependency changes in Rclone, run `go mod vendor` in the tarball's source directory. Use [flatpak-go-mod](https://github.com/flatpak/flatpak-builder-tools/tree/master/go-modules) to regenerate `go.mod.yml` and save it as `go-sources.yml`. Make sure to copy over the updated `modules.txt` as well.
- Run `./flatpak-build.sh` to do a local test build. This script is not used by Flathub's build system.
