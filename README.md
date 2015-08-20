upwn Version 1.1 Update Tutorial

If You Follow This Guide To The Letter You Should Be Able To Update Binary To Support Other Device Models, IPSW Firmware Versions for downloading and Key/IV for respective downloaded firmware


#1 Grab The HTML Download Link For The IPSW From https://www.theiphonewiki.com/wiki/Firmware
OR
https://ipsw.me
And Replace the cURL Link In /usr/bin/upwn.sh like the example below 
EXAMPLE
"curl -O http://ipsw_link_goes_here"


#2 Get The Exact Names Of desired IPSW File Contents and Revise The names and Directories in the /usr/bin/upwn.sh binary 
For the xpwntool File In And File Out 
As well as updated directories "if needed"
Like the example below
EXAMPLE
"000.0000.000.dmg"
OR
"Apple.Logo.IMG3"
OR
"IPSW/Firmware/dfu/blah.img3"

#3
This Is The Last but Very Crucial Step, Each and Every IPSW has a Diffrent Key and IV for each of its perspective components 
"Except for ancient 8200 devices"
You Need To Copy and Paste "for now" Each Key and IV for each perspective part of the firmware in the /usr/bin/upwn.sh binary
Like so below 
EXAMPLE
"-k asdfghjklasdfghjklasdfghjklasdfg"
"-iv asdfasdfasdfasdf"
NOTE Key will always be longer than the IV and RootFS "regardless of Device model" will ONLY have a key and NO IV,  xpwntool will not work for decryption which is why dmg is used instead with only a key 
