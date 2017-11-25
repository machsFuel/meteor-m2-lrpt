# meteor-m2-lrpt
GNU Radio scripts for METEOR M2 Satellite LRPT reception with AIRSPY SDR.


These scripts require GNU radio 3.7.x - older versions of GNU radio will not work due to missing blocks.

These GRC flow graphs provide a realtime LRPT Soft-Symbol Receiver.

Original author of base script: Martin Blaho (modified by Raydel Abreu for RTL SDR)
Modification for Airspy: by Otti (decimating FIR, RRC filtering)
Modification for rtl dongles and command line operations: by machsFuel

I hacked up Otti's GRC flow graphs to work from the command line for easier scheduling.  There is a single input variable for the output file name.  The output is a .s file which works with artlav's meteor_decoder tools. 

Usage::
skywave.py --destfile filename
