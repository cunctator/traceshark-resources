SAMPLE TRACES II

The use case in all these traces is opening the same large file with
traceshark. So the idea behind these traces is to use traceshark in order to
study the behevior of traceshark itself.

All files are compressed with xz and need to be decompressed like this:

xz -dc file_to_open_with_traceshark.asc.xz > file_to_open_with_traceshark.asc

4cpu-diskload/file_to_open_with_traceshark.asc:

 * This trace is on a 4 CPU system.
 * The file was not present in the buffer cache, so the kernel has to load the
   file from an SSD with SATA interface.

4cpu-ramload/file_to_open_with_traceshark.asc:

 * This trace is on a 4 CPU system.
 * The file was already present in the buffer cache, so no loading
   from SSD happens.

8cpu-diskload/file_to_open_with_traceshark.asc:

 * This trace is on a 8 CPU system.
 * The file was not present in the buffer cache, so the kernel has to load the
   file from an SSD with SATA interface.

8cpu-ramload/file_to_open_with_traceshark.asc:

 * This trace is on a 8 CPU system.
 * The file was already present in the buffer cache, so no loading
   from SSD happens.
