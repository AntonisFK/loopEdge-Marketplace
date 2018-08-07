# DeviceHub Speed Tester

This application is used to test performance of DeviceHub to Southbound devices communication.

## Usage

This application is designed to subscribe data from devicehub and show statistics of the communication.

command field is defined as per below:

**NAME:**

   natstool - LoopEdge DST Tool

**USAGE:**

   natstool [global options] command [command options] [arguments...]

**COMMANDS:**

     grub     start grubbing mode

     gen      start generate mode

     help, h  Shows a list of commands or help for one command

**GLOBAL OPTIONS:**

   --debug, -d          enable verbose logging [$LOOPEDGE\_NATS\_TOOL\_DEBUG]

   --log-format format  log format (&quot;text&quot;, &quot;json&quot; or &quot;term&quot;) (default: &quot;term&quot;) [$LOOPEDGE\_NATS\_TOOL\_LOG\_FORMAT]

   --nats-url value     DataHub or NATS server URL (default: &quot;nats://localhost:4222&quot;) [$LOOPEDGE\_NATS\_TOOL\_NATS\_URL]

   --help, -h           show help

   --version, -v        print the version

COPYRIGHT:

   (c) 2018 Litmus Automation Inc.

**Examples**

1. To print data for a specific PLC

./natstool grub – -topic=&quot;devicehub.raw.deviceid.\&gt;&quot; – -print

1. To print data for a specific tag

./natstool grub – -topic=&quot;devicehub.raw.deviceid.\&gt;&quot; – -contains=&quot;tagname&quot; - -print

1. To print all data coming from all connected PLC

./natstool grub – -topic=&quot;devicehub.raw.\&gt;&quot; –print

1. To measure number of messages in x seconds

./natstool grub – -topic=&quot;devicehub.raw.deviceid.\&gt;&quot; –stat\_timer=x

1. To print tags having false values

./natstool grub – -topic=&quot;devicehub.raw.deviceid.\&gt;&quot; – -contains=&quot;false&quot; - -print

1. To save all the tags in a text file

./natstool grub – -topic=&quot;devicehub.raw.deviceid.\&gt;&quot; –print \&gt; /tmp/filename.txt
