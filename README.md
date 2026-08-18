# Cell-Offset-Generator

Cell-offset table generator for Bethesda games. Speeds up ESP cell lookups by extending the OFST fast-path beyond masters — regenerates worldspace cell offset tables that tools like xEdit strip out.

> Fork of [1001Bits/Cell-Offset-Generator](https://github.com/1001Bits/Cell-Offset-Generator).

## Layout

| Directory | Game | Notes |
| --- | --- | --- |
| `Skyrim/` | Skyrim SE/AE | SKSE plugin, CMake presets (`vs2022-windows-vcpkg`, …), CommonLibVR submodule under `extern/` |
| `Fallout 4/` | Fallout 4 | F4SE variant |
| `Starfield/` | Starfield | SFSE variant |

## Building (Skyrim)

Requirements: Visual Studio 2022 (C++ workload), CMake 3.21+, vcpkg (`VCPKG_ROOT` set). Clone with submodules:

```powershell
git clone --recurse-submodules <this-repo>
cd Skyrim
cmake --preset vs2022-windows-vcpkg
cmake --build build --config Release
```

## License

See [LICENSE](LICENSE).
