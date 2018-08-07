# Python

This application is used to test performance of DeviceHub to Southbound devices communication.

## Usage

This application is designed to subscribe data from devicehub and show statistics of the communication.

command field is defined as per below:

```
Examples
```
1.	To print data for a specific PLC
./nats_tool grub – -topic=”devicehub.raw.deviceid.>” – -print
2.	To print data for a specific tag
./nats_tool grub – -topic=”devicehub.raw.deviceid.>” – -contains=”tagname” - -print
3.	To print all data coming from all connected PLC
./nats_tool grub – -topic=”devicehub.raw.>” –print
4.	To measure number of messages in x seconds
./nats_tool grub – -topic=”devicehub.raw.deviceid.>” –stat_timer=x 
5.	To print tags having false values
./nats_tool grub – -topic=”devicehub.raw.deviceid.>” – -contains=”false” - -print
6.	To save all the tags in a text file 
./nats_tool grub – -topic=”devicehub.raw.deviceid.>” –print > /tmp/filename.txt

```
```
