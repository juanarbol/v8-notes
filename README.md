# V8 Notes

## Table of contents
  * [Getting the source code](#getting-the-source-code)
  * [Installing `depot_tools`](#installing-depot_tools)

### Getting the source code

For getting v8's source, first, update [`depot_tools`](#installing-depot-tools) by running:

`$ gclient`

After `depot_tools` is updated, the missing part is decide a place to save v8 (folder in your filesystem) and run `fetch` command:

```sh
mkdir /path/for/chromium/
cd /path/for/chromium/
fetch v8
cd v8
# Update third party deps of v8
gclient sync
```

Ok, let's be real, this could take like WHILE (hm, a looonnnggg one), so, be prepared to be patient.

_References:_
  * [Chromium docs](https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html#_setting_up)
  * [V8 docs](https://v8.dev/docs/source-code)

### Installing `depot_tools`

The `depot_tools` are just tooling for git operations of the Chromium project.

#### Installing `depot_tools` on Linux/macOS

Open a terminal, and move to the folder that `depot_tools` will be installed and clone the repo:

`$ git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git`

After clonning the `depot_tools` repository (this is just for better development experience, optional), add the `depot_tools` to `PATH`:

`$ export PATH=/path/to/depot_tools:$PATH`

