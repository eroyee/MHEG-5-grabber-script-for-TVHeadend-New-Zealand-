This script collects and assembles DVB-T MHEG-5 EPG data from a DVB demux device, it then creates an 
XML output that is imported to TVHeadend via the 'Internal XMLTV grabber' facility.

Options are available to write the resultant XML data to a file, and to use a config file in order
to specify the collected channels, and their naming convention. By itself the script will auto-name
and collect all the available channels, you can then determine those you wish to use within TVH.

In addition to the auto-collection I have written this to conform, more or less, to the XMLTV grabber requirements,
(https://wiki.xmltv.org/index.php/XmltvCapabilities) so it *may* work with other systems that use this convention.
That said, and because they don't seem to be needed in my application, the 'capabilities' are limited. Should it
prove necessary they could be implemented.

Importantly this has also been coded to avoid disk writes, which should assist in preserving SD-cards if 
this is use in the likes of a RPi for example.

No internet is required, the point of this is to be completely independent of the 'net. If you're able
to receive terrrestrial broadcasts it should be able to extract the requisite EPG data, with the 
proviso that a good signal will assist in reducing errors.

Configuration should not be required for it to 'just work'. Simply place the file wherever your tv_grab*
files should be ('/usr/bin/' maybe) and TVH should pick it up...
