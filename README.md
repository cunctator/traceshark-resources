# traceshark-resources

This is a repository intended for sharing some example files and documentation for traceshark. I put these in a separate repository because I don't want to pollute the traceshark repository with a lot of binary files that are not strictly necessary.

You can find traceshark here:
[https://github.com/cunctator/traceshark](https://github.com/cunctator/traceshark])

# Contents

Currently, the only thing available in this repository is:
 * Four sample traces in [sample-traces2](https://github.com/cunctator/traceshark-resources/tree/master/sample-traces2). These sample traces were obtained with perf when opening a large, circa 2GB, trace with traceshark.
 * A [README.txt](https://raw.githubusercontent.com/cunctator/traceshark-resources/master/sample-traces2/README.txt) that describes the traces.
 * There is a screenshot for each trace, to show what it is supposed to look like.

# How to use

You only need to unpack the files ending with .asc.xz like this:
```
xz -dc xz -dc file_to_open_with_traceshark.asc.xz > file_to_open_with_traceshark.asc
```

The output file is the one that you open with traceshark. For more info about how to use traceshark, see the traceshark repository:
[https://github.com/cunctator/traceshark](https://github.com/cunctator/traceshark])

# What is it supposed to look like in traceshark?

If you use KDE and have a monitor with non-standard 1920x1920 resolution, you should see something like this:
![Screenshot of traceshark](https://raw.githubusercontent.com/cunctator/traceshark-resources/master/sample-traces2/4cpu-ramload/screenshot.png)
