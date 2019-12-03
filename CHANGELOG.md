## Release 0.6.0 (2019-12-03)
```
Changes:

  + 6882689:
    Compare mode for actions with output directories.
  + 08499f0:
    Add flag to enable shadow header detection.
  + 709061a:
    Switching SDK to latest commit (retries)
  + 04eb160:
    Add a tool action type to run any tool with the inputs/outputs
  + f6cc51b:
    Add reproxy version number as a cache silo to all actions.
  + 0519b5b:
    Move flags structs to a separate package: pkg/flags.
  + c16f9c8:
    Simplify the signature of ProcessInputsShallow.
  + 1165068:
    Fix flaky test due to non-deterministic order of include directories.
  + 4ff0a4b:
    Optimize shadow headers performance.
  + 04223fe:
    Refactor runLERC code to follow go readability guidelines.
  + 4087961:
    Switching to latest SDK version
  + be22f0b:
    Add documentation about the dependency scanner plugin
  + 996339d:
    Change V(2) log to warning log when RE fails and we fallback to local
  + 689c6cb:
    Update foundry-vars.sh to the correct instance name.
  + d8bcce5:
    Make rewrapper retries less aggresssive and increase max retry duration
  + 356debf:
    Fixing stats aggregation bug.
  + 222117f:
    Pass rewrapper start time to reproxy for logging and aggregation.
  + b6b1478:
    Restrict input processor parallelism to num CPU cores
  + 7b54918:
    Adding include processor timing stats.
  + fe28910:
    Adding end-to-end timing stats, minor refactoring
  + 9c1afd7:
    Adding local execution timing stats to the proxy
  + 2cac73d:
    Rename rbe_metrics file to rbe_metrics.txt
  + 82edf55:
    Adding LERC deps timing metadata
  + 50d62ad:
    Add dependency scanner plugin to the release script
```

This release adds local performance metrics and shadow header detection as an
off by default feature.

## Release 0.5.3 (2019-11-13)
```
Changes:

  + da676b7:
    Statically link libstdc++ with the Go plugin to avoid
    libstdc++ version issues on Android buildbot.
```

This release addresses libstdc++ loading issue on dependency scanner plugin.

## Release 0.5.2 (2019-11-13)
```
Changes:

  + 7a4cc47:
    Don't fail reproxy when loading of dependency scanner plugin fails.
  + efea8bf:
    Add a temporary workaround suggested in rules_go to fix issue
    with version number stamping.
```

This release makes reproxy not fail when it cannot load CPP dependency
scanner plugin.

## Release 0.5.1 (2019-11-11)
```
Changes:

  + 05875af:
    Add dependency_scanner_go_plugin.so to Kokoro regex too
```

This release makes the Kokoro workflow also upload dependency scanner
plugin.

## Release 0.5.0 (2019-11-11)
```
Changes:

  + 2904c9d:
    Implementing LERC with include directories awareness for constructing
    dependency file.
  + 2c7f757:
    Migrating to latest dependency versions and Bazel 1.1.
  + cc8cc63:
    Wire up clang-scan-deps to input processor.
  + 13374fc:
    Adding output metrics and digests to proxy log and stats.
  + a46e81f:
    Support rsp files for javac compiles.
```

This release mainly adds dependency scanner plugin to support remote execution
for C++ compile actions.

## Release 0.3.0 (2019-10-22)
```
Changes:

  + ba1466e:
    Add flag to control bootstrap timeout
  + 55d0ad6:
    Keep track of RBE tool version in Dremel
  + 3839b37:
    Renaming Dial to NewClient for clarity
```

This release mainly adds RBE tool version number to dumpstats.
