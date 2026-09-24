# gstreamer-sharp-1.29.1

.NET / Mono bindings for GStreamer, generated from gobject-introspection data with bindinator. This is the gstreamer-sharp 1.29.1 tree (unstable 1.29 development line toward 1.30), wrapping core and base GStreamer APIs plus GES, with C# samples and meson/MSBuild build support. Upstream project; this repo is my working copy.

**Source last updated:** 2026-04-04 · **Language:** C# · **Framework:** .NET Framework 4.8 (also meson/mono) · **Output:** Class library (`gstreamer-sharp`) plus samples and tests

## Solution structure

| Project / area | Language | Type | Purpose |
|---|---|---|---|
| gstreamer-sharp | C# | Class library | Core GStreamer .NET bindings (custom + generated) |
| sources / ges | C# / C | Generated bindings | Gst and GES API wrappers |
| samples | C# | Sample apps | Ports of gst-docs tutorials and playback examples |
| Tests | C# / Python | Tests | App, SDP, and ABI tests |
| meson / nuget scripts | Python / Meson | Build | Meson build, NuGet packaging, code generation |

## How to open

- Visual Studio: open `gstreamer-sharp.sln` (or `gstreamer-sharp.csproj` targeting .NET Framework 4.8).
- Meson: `meson build && ninja -C build/` (see also `README.upstream.md`).

## Requirements

- Visual Studio 2013 to 2022 (ToolsVersion 12.0 / TargetFrameworkVersion v4.8), or Mono (`mcs` / `al`) for meson builds
- .NET Framework 4.8 (MSBuild path); meson path needs mono-devel
- GStreamer core/base/good 1.14 or higher
- gtk-sharp 3.22.0 or higher (can build as a meson subproject)
- Meson and Ninja for the upstream build path

## Attribution and provenance

Original project: gstreamer-sharp (GStreamer / mono GSoC 2014 lineage), licensed under LGPL 2.1 — see `COPYING` and `README.upstream.md`.

Working copy from my Development folder `gstreamer-sharp-1.29.1`.

## License

LGPL 2.1 (upstream). See `COPYING`. This working copy retains the original license; it is not re-licensed under MIT.
