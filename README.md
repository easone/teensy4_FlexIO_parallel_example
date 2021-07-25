# teensy4_FlexIO_parallel_example

On Teensy 4, FlexIO allows you to output parallel data to 4 pins (or 8, 16, or 32) and have it clocked out at a precise frequency. FlexIO2 pins 0-3 are available on T4.

The way FlexIO works is that you transfer your data to a series of buffered shift registers (up to 128 bits wide) and then it automatically shifts out to your output pins 4 bits at a time. You can load the buffers with DMA or just with normal register accesses.

This example code shifts out data in parallel to pins 10-13 every 25 ns. In the latest version of Teensyduino (1.54), it requires no external libraries. 

Here's an oscilloscope screenshot with channels 1,2,3,4 hooked to pins 10,12,11,13:
