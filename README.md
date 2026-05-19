# scoop-personal

Personal [Scoop](https://scoop.sh) bucket for Windows apps that are not in [main](https://github.com/ScoopInstaller/Main) or [extras](https://github.com/ScoopInstaller/Extras).

[![CI](https://github.com/obfuscated-loop/scoop-personal/actions/workflows/ci.yml/badge.svg)](https://github.com/obfuscated-loop/scoop-personal/actions/workflows/ci.yml)
[![Excavator](https://github.com/obfuscated-loop/scoop-personal/actions/workflows/excavator.yml/badge.svg)](https://github.com/obfuscated-loop/scoop-personal/actions/workflows/excavator.yml)

## Install bucket

```
scoop bucket add personal https://github.com/obfuscated-loop/scoop-personal
```

## Apps

| App | Description |
| --- | --- |
| [minimalimageviewer](bucket/minimalimageviewer.json) | Lightweight image viewer with OCR and basic editing |

## Add a new app

1. Copy `bucket/app-name.json.template` to `bucket/<app-name>.json`.
2. Fill in `version`, `url`, `hash`, `description`, `homepage`, and `license`.
3. Add `checkver` / `autoupdate` when the upstream publishes releases.
4. Open a PR or push to `master`; CI runs bucket tests.

Update manifests locally:

```powershell
scoop checkver -d bucket minimalimageviewer
scoop checkver -d bucket minimalimageviewer -u
```

## License

Manifests and bucket metadata are dedicated to the public domain ([Unlicense](LICENSE)). Individual apps keep their upstream licenses (see each manifest’s `license` field).
