# LogstashConfLoggen
this is a config logstash file for parsing and filtering loggen generated syslogs.

**NOTE**: The loggen application is distributed with the syslog-ng system logging application, and is usually part of the syslog-ng package. The loggen application is tool to test and stress-test your syslog server and the
       connection to the server. It can send syslog messages to the server at a specified rate,
       using a number of connection types and protocols, including TCP, UDP, and unix domain
       sockets. The messages can be generated automatically (repeating the PADDstring over and
       over), or read from a file or the standard input.
<br>
for more information you can check [loggen documentatio]n(http://manpages.ubuntu.com/manpages/bionic/man1/loggen.1.html)
<br>
loggen generated syslog example:
```
<38>2020-04-02T23:45:20 localhost prg00000[1234]: seq: 0000000005, thread: 0000, runid: 1585854915, stamp: 2020-04-02T23:45:20 PADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADDPADD
```
this config file **,only accepts even seq numbers**, therefore it doesn't accept the example above.
