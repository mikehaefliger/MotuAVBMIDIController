# Motu AVB MIDI Controller

Control the Motu AVB mixing console with any MIDI controller. The translation from CC to OSC is created with the help of Pure Data and is a one-way connection. Nevertheless, MIDI CCs are establishing a complete two-way connection for recall functions. The autosave function saves the main patch and the subpatches every 30 seconds.

**Tested with**
- Motu LP32
- RaspberryPi 3 Model B+ with PD installed
- Electra One MkII v3.6.1

**Requirements**
- Any Motu AVB Interface with Mixing Console
- Pure Data (PD 0.55.2)
- MIDI Controller

# Instructions
1. Connect Motu AVB Interface via Ethernet
2. Ensure PD-Device and Motu Interface have a valid IP address
3. Setup Pure Data MIDI-Settings
4. Open "lp32-avb.pd" file in Pure Data
5. Change "connect lp32.local 9998" with the IP from your Motu interface
6. Change MIDI Settings (MIDI Channel and CC#) in the subpatch "avb_midi_settings"

Except for reverb and main mix, all mixing channels share the same MIDI CC numbers. Use the channel selector to change the individual channels (MIDI CC#20, Value 1-18).
