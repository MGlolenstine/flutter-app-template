# flutter-app-template [![Join Gitter Chat Channel](https://badges.gitter.im/flutter-rs/community.svg)](https://gitter.im/flutter-rs/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


Example app built using flutter-rs.
 <img src="https://raw.githubusercontent.com/gliheng/flutter-rs/master/www/images/logo.png" width="50" height="50" align="center" />

![screenshot](https://raw.githubusercontent.com/gliheng/flutter-rs/master/www/images/screenshot_mac.png)


- Runs on mac and linux, so far.
- Build distribution only works on mac.
- Windows will be supported.

# Requirement

- [Rust](https://www.rust-lang.org/tools/install)
- libglfw:
    - Install on Mac with: `brew install glfw`
    - Install on linux with `apt install libglfw3`

# Get Started
## Clone

    git clone git@github.com:gliheng/flutter-app-template.git flutter-app
    cd flutter-app
    ./scipts/init.py

## Config
- Set flutter engine version in *Cargo.toml*

```
[package.metadata.flutter]
version = "5af435098d340237c5e3a69bce6aaffd4e3bfe84"
```

    This commit version id can be found in bin/internal/engine.version file in flutter sdk folder.

## Develop

- To develop with hot-reloading, use:
    `./scripts/run.py`

    To show rust logs, add these environment variables: `RUST_LOG=flutter_engine=trace,flutter_app=trace ./scripts/run.py`

## Distribute

- To build distribution, use:
    `./scripts/build.py mac`
    `./scripts/build.py dmg`

**Note:**
Build scripts are written in python3. Install python depenendencies using `pip3 install -r scripts/requirements.txt`

---

### For users in China
Please ensure you have access to *storage.googleapis.com*. It is required to download lib_flutter. 

Set appropriate http proxy in the terminal by using:
```shell
export http_proxy=...
export https_proxy=...
```