# Spartacus Changelog

## v2.2.0

* `[New]` Included `Examples.md` in the distribution archive.
* `[New]` As command line arguments were becoming too much, created `CommandLineGenerator.html`.
* `[New]` Implement the `sign` mode, to enable creating self-signed certificates and using any given certificate to sign an executable/DLL. The code was taken & customised from https://github.com/Danielku15/SigningServer, under MIT License - original author is Danielku15.
* `[Fix]` Fixed PostBuildEvent in proxy.vcxproj, [PR](https://github.com/Accenture/Spartacus/pull/3) by https://github.com/Signum21.
* `[Fix]` Fixed placeholder creation when DLL does not exist, [PR](https://github.com/Accenture/Spartacus/pull/6) by https://github.com/kost.

## v2.1.3

* `[Update]` Proxy `--action exports` now supports wildcard DLL paths like `--dll C:\Windows\System32\*.dll` and also displays forwarded functions.
* `[Fix]` Rewrite PE file exporter from scratch.

## v2.1.2

* `[New]` Added `--action exports` to `--mode proxy` that lists a file's exports, functionality similar to `dumpbin.exe /exports`.
* `[Fix]` Fixed `--only` parameter which was ignored when generating a proxy solution without using Ghidra.

## v2.1.1

* `[Update]` Added support for `NTAPI` prototypes.

## v2.1.0

* `[New]` Added `--action prototypes` to `--mode proxy` that supports the parsing of `*.h` files in order to generate pre-existing function prototypes.
* `[New]` Included `./Assets/prototypes.csv` with a pre-generated list of function prototypes.
* `[Update]` Updated `--mode com --acl` functionality to check the parent folder's permissions as well when checking for misconfigured COM registry entries.

## v2.0.0

* `[New]` Implement support for identifying COM Hijacking.
* `[New]` Added option to support external resources for solution generation.
* `[Update]` Improve Visual Studio solution generation.
* `[Update]` Simplified and reduced command line arguments.
* `[Removed]` Removed the individual `*.cpp` proxy skeleton file generation, replaced with full solutions.

## v1.2.0

* `[New]` Implement replication of `VERSIONINFO` and timestomping to match source file during solution compilation. (Issue #1)

## v1.1.1

* `[Fix]` Allow digits/symbols in --only-proxy command

## v1.1.0

* `[New]` Implement new functionality to create proxies for functions other than DllMain, as described here: https://www.redteam.cafe/red-team/dll-sideloading/dll-sideloading-not-by-dllmain

## v1.0.0

* `[New]` Public Release.
