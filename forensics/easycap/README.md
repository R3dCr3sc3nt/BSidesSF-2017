# easycap

## Challenge

> Can you get the flag from the packet capture?

> [easycap.pcap](easycap.pcap)

## Solution

I started by opening up the file in [Wireshark](https://www.wireshark.org/). After some browsing around in the UI, I finally clicked on Analyze > Follow > TCP Stream. Here I was greeted with the flag: `FLAG:385b87afc8671dee07550290d16a8071`.
