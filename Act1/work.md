#Questions 

## Was the server compromised? If so, how? If not, what happened? What needs to happen before the system is put back into service?

Yes, 

#What we know 
- Bob lab's server was infected with a worm 
- The NOC determined this because of a huge spike in Internet traffic which occurred at 4 in the morning.
- He immediately shut it down and brought it in to be imaged.
- There were hardly any files on it except for his own account 'bob' and some student accounts 'eric', 'kevin', 'peter' and 'takeda'.

##Questions:

- Was the server compromised? 
- If so, how? If not, what happened? 
- What needs to happen before the system is put back into service?



#System Logs and Process Accounting


##Auth.log 

- Jan  4 08:55:47 server sshd[2375]: Accepted password for kevin from 192.168.56.1 port 42660 ssh2
- Jan  4 08:56:04 server sshd[2392]: Accepted password for takeda from 192.168.56.1 port 42661 ssh2
- Jan  4 08:56:06 server sshd[2412]: Accepted password for eric from 192.168.56.1 port 42664 ssh2
- Jan  4 08:57:39 server sshd[10534]: Accepted password for eric from 192.168.56.1 port 42711 ssh2
- Jan  4 09:00:25 server sudo:      bob : TTY=tty1 ; PWD=/home/bob ; USER=root ; COMMAND=/sbin/shutdown -h now

##syslog


#USER 

##BOB 

- .bash_history => sudo shutdown -h now

##ERIC 

- .bash_history => mutt logout (repeated many times)

##KEVIN 

- .bash_history =>

##PETER 

- .bash_history => 

##TAKEDA





-- Methodology 

Something like this would be good to have here:

The software and shell tools used in the investigation are as follows: 
sha256sum – displays the SHA256 hash of a file. 
e2undel / scalpel – recovers deleted files. 
chkrootkit - checks the system for known rootkits. 
cd – changes and navigates through directories. 
less – displays contents of a text file. 
grep - searches a file for matching strings. 
stat – displays detailed information relating to a file or file system.

The disk image was obtained on the 11th of February 2020, at 13:01,
GMT+1. The actions below were performed between February 11 2020,
13:01 and February 11 2020, 17:30, GMT+1, with additional work per-
formed on March 4 2020, between 18:00 GMT+1 and 19:30 GMT+1.













