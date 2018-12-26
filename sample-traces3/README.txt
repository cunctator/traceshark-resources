SAMPLE TRACES III

The use case in all these traces is opening the same large file with
traceshark. So the idea behind these traces is to use traceshark in order to
study the behavior of traceshark itself. The difference between these traces
is mainly the number of CPUs, how the SSD is connected to the computer, and
whether the file was already present in the buffer cache or not.

All files are compressed with xz and need to be decompressed like this:

xz -dc file_to_open_with_traceshark.asc.xz > file_to_open_with_traceshark.asc

4cpu-ramload/file_to_open_with_traceshark.asc:

 * This trace is on a 4 CPU system, 2 physical and 4 virtual CPUs.
 * The file was already present in the buffer cache, so no loading
   from SSD happens.

4cpu-sata/file_to_open_with_traceshark.asc:

 * This trace is on a 4 CPU system, 2 physical and 4 virtual CPUs.
 * The file was not present in the buffer cache, so the kernel has to load the
   file from an SSD through the SATA interface.

8cpu-nvme/file_to_open_with_traceshark.asc:

 * This trace is on a 8 CPU system, 4 physical and 8 virtual CPUs.
 * The file was not present in the buffer cache, so the kernel has to load the
   file from an SSD through the PCIe interface.
 * However, in this case the SSD is so fast that it is  faster than what
   traceshark can consume data, so it looks quite similar to the ramload cases.

8cpu-ramload/file_to_open_with_traceshark.asc:

 * This trace is on a 8 CPU system, 4 physical and 8 virtual CPUs.
 * The file was already present in the buffer cache, so no loading from SSD
   happens.

8cpu-usb/file_to_open_with_traceshark.asc:

 * This trace is on a 8 CPU system. 4 physical and 8 virtual CPUs.
 * The file was not present in the buffer cache, so the kernel has to load the
   file from an SSD through the USB interface.
