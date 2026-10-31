#
dmesg shows it is a linux deivce. I was not able to get a response on 
/dev/ttyACM0, nor the network.  screen blanks after boot. didnt feel like messing with it.

```dmesg
l@cker:~/HMIs/HORNER/XL4_OCS_model6$ sudo dmesg -w
[ 9457.153511] r8169 0000:02:00.0 enp2s0: Link is Down
[ 9459.488797] usb 1-2: USB disconnect, device number 10
[ 9459.960030] r8169 0000:02:00.0 enp2s0: Link is Up - 100Mbps/Full - flow control off
[ 9467.188081] usb 1-2: new high-speed USB device number 11 using xhci_hcd
[ 9467.319169] usb 1-2: New USB device found, idVendor=1e58, idProduct=0001, bcdDevice=24.26
[ 9467.319184] usb 1-2: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[ 9467.319190] usb 1-2: Product: Gadget Serial v2.4
[ 9467.319195] usb 1-2: Manufacturer: Linux 2.6.35.3-571-gcca29a045 with fsl-usb2-udc
[ 9467.324494] cdc_acm 1-2:2.0: ttyACM0: USB ACM device
[ 9469.101406] r8169 0000:02:00.0 enp2s0: Link is Down
[ 9471.855464] r8169 0000:02:00.0 enp2s0: Link is Up - 100Mbps/Full - flow control off

```
