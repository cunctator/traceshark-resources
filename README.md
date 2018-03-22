# traceshark-resources

This is a repository intended for sharing some example files and documentation for traceshark. I put these in a separate repository because I don't want to pollute the traceshark repository with a lot of binary files that are not strictly necessary.

You can find traceshark here:
[https://github.com/cunctator/traceshark](https://github.com/cunctator/traceshark])

# Contents

Currently, the only thing available in this repository is:
 * A sample trace in [sample-traces/traceshark-opening-large-file.asc.xz](https://raw.githubusercontent.com/cunctator/traceshark-resources/master/sample-traces/traceshark-opening-large-file.asc.xz). This sample trace was obtained with perf when opening a large, circa 1.5GB, trace with traceshark.
 * A [screenshot](https://raw.githubusercontent.com/cunctator/traceshark-resources/master/sample-traces/traceshark-opening-large-file.png) of how it would/could/should look like.

# How to use

You only need to unpack the file like this:
```
xz -dc sample-traces/traceshark-opening-large-file.asc.xz > sample-traces/traceshark-opening-large-file.asc
```

The output file is the one that you open with traceshark. For more info about how to use traceshark, see the traceshark repository:
[https://github.com/cunctator/traceshark](https://github.com/cunctator/traceshark])

# What is it supposed to look like in traceshark?

If you use KDE and have a monitor with non-standard 1920x1920 resolution, the sample file should look something like this:
![Screenshot of traceshark](https://raw.githubusercontent.com/cunctator/traceshark-resources/master/sample-traces/traceshark-opening-large-file.png)
