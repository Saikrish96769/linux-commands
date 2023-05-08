# Linux basics

## File management:

### ls command:
The ls command is a basic Unix command that is used to list the files and directories in a specified directory. By default, when you run the ls command without any arguments, it will list the files and directories in the current working directory. 

#### syntax : 
- 
```
ls -(options)
```

Here are some common options that can be used with the ls command:

- -a: Lists all files, including hidden files that start with a dot (.)
- -l: Displays the files in a long format, which includes permissions, ownership, size, and modification time.
- -h: Displays the file sizes in a human-readable format, such as KB or MB.
- -r: Reverses the order of the list.
- -t: Sorts the list by modification time, with the newest files first.
- -R: Lists all files and directories recursively, starting from the current directory.

### Cat command:
Used to concatenate and display contents of one or more files.

#### syntax :
-
```
cat [options] [file(s)]
```
To display the contents of multiple files, you can list them all as arguments to the cat command:

#### syntax :
-
```
cat [file1] [file2] [file3]
```

Here, options refer to various command line options that can modify the behavior of the cat command, and file(s) refer to one or 
more files whose contents will be displayed.

#### Some common options for the cat command include:
- -n: display line numbers for each line
Usage: 
```
cat -n [filename]
```             
 output:1 (text in first line).

- -b:display line numbers for non-blank lines only 
Usage:
```
cat -b [filename]
```
output:
1 (text in first line).
  (text in blank line).

- -s: squeeze multiple adjacent blank lines into a single blank line.
Usage:
```
cat -s [filename]
```
output:
Squeezes blank lines to one.

- -v: display non-printable characters as escape sequences.
Usage:
```
cat -v [filename]
```
output:
display non-printable characters as escape sequences.

### Tail command:
The tail command is a command-line utility in Unix-based operating systems that is used to display the last few lines of a file. By default, it displays the last 10 lines of a file, but this can be changed using command options.

#### syntax of the tail command:
-
```
tail [options] [file(s)]
```
Here, [options] are the various command options that can be used with tail, and [file(s)] is the name of the file(s) that you want to display the last few lines of.

Some common options that can be used with the tail command are:

- -n N: Specifies the number of lines to display from the end of the file. 

For example, 
```
tail -n 5 file.txt
``` 
will display the last 5 lines of the file file.txt.

- -f: Allows the tail command to continue running and display any new lines that are added to the file in real-time. This is useful for monitoring log files or other constantly-updating files.

### locate command:
The locate command is a Linux/Unix command-line tool used to find files by name. It searches a pre-built database of file names and their paths, which makes it faster than searching the file system directly.

To use the locate command, open a terminal and type:

#### syntax:
-
```
locate [filename or pattern]
```
#### For example, to find all files with the word "example" in their name, you would type:
-
```
locate example
```
Note that the locate command requires a pre-built database, which is usually updated daily by a cron job. If you need to find a file that was recently created or modified, you may need to run the updatedb command to update the database before using locate.

### cd command:
The cd command is a command-line interface (CLI) command used to change the current working directory in a shell or terminal.

#### The syntax for using the cd command is:
-
```
cd [directory]
```
where [directory] is the name of the directory you want to change to. If [directory] is not specified, then cd will take you to your home directory.

Here are some common examples of how to use the cd command:

- Change to the root directory:
#### syntax:
-
```
cd /
```

- Change to the home directory:
#### syntax:
-
```
cd ~
```
- Change to a directory named "Documents" in your current directory:
#### syntax:
-
```
cd Documents
```

- Change to the parent directory:
#### syntax:
-
```
cd ..
```
- Change to the previous directory you were in:
#### syntax:
-
```
cd -
```
### Touch command:
It is used to create an empty file or update the modification and access times of an existing file.

#### syntax for the touch command is:
-
```
touch [options] filename(s)
```

#### Some common options for the touch command include:
- -a: Only update the access time of the file(s).
- -c: Do not create any files. If a specified file does not exist, no error message is displayed.
- -m: Only update the modification time of the file(s).
- -r: Use the access and modification times of a reference file.
- -t: Specify a specific time to set the access and modification times.

#### Example, To create a new file named "file.txt":
```
touch file.txt
```
#### To set the access and modification times of a file to a specific date and time:
```
touch -t 202105031230.30 file.txt
```

### mkdir command :
That is used to create a new directory or folder.

#### The basic syntax for the mkdir command is:
````
mkdir [options(-m -p -v)] directory-name(s)
````
- -m: Set the file mode (permissions) of the created directory to the specified mode.
```
mkdir -m 755 my_directory
```
- -p: Create the parent directories as needed. If any of the parent directories do not exist, they are created as well.
```
mkdir -p parent_directory/my_directory
```
- -v: Display a message(directory name) for each directory that is created.

### mv command:
That is used to move or rename files and directories.

#### The basic syntax for the mv command is:
```
mv [options] source(s) destination
```
#### options:
- -i: Prompt the user before overwriting an existing file.
- -f: Force the move, even if it would overwrite an existing file without prompting.
- -n: Do not overwrite an existing file.
- -v: Display a message for each file that is moved.

- rename
```
mv file.txt new_file.txt
```

- To move a file from the current directory to a subdirectory called "my_directory":
```
mv file.txt my_directory/
```
- To move a file and overwrite an existing file without prompting:
```
mv -f file.txt my_directory/file.txt
```
- To move a file and display a message:
```
mv -v file.txt my_directory/
```
- To move a directory and all of its contents to a new location:
```
mv directory/ new_location/
```
### rm, rmdir command:
That is used to remove files or directories.

#### The basic syntax for the rm command is:
```
rm [options] file(s) or directory(s)
```
options:
- -i: Prompt the user before removing each file or directory.
- -r: Remove directories and their contents recursively.
- -f,rf: Force the removal without prompting(file, directory).
- -v: Display a message for each file or directory that is removed.

### vi command:
 It is a modal editor, meaning it has different modes for inserting text, navigating the document, and performing other tasks.

#### The basic syntax for the vi command is:
```
vi filename
```
#### Some common commands and shortcuts for vi include:

- i: Switch to insert mode.
- esc: Return to command mode.
- :w: Save the document.
- :wq: Save and quit, :wq!: save and quit without conformation.
- :q: Quit without saving (if there are no unsaved changes).
- :q!: Quit without saving, discarding any changes.
- To delete a line of text and move cursor to below deleted line we use 'dd' or simply 'd' for deleting (one or more)line.
#### To search for a word in vi editor, you can use the following command while in command mode:
:/word , :?\word(backward search).

#### regular expressions(example of  all occurrences of the word "example" followed by a numbe):
:/example\d

### cp command:
The cp command is a command-line utility in Unix and Unix-like operating systems that is used to copy files or directories from one location to another. 

#### The basic syntax of the cp command is as follows:
````
cp [options] source_file destination
````
#### examples:
- cp file1.txt folder/ (current to folder)
- cp /path/to/file1.txt /path/to/destination/(one to another)
- cp -r folder1/ folder2/ (all contents from one folder to another)
- cp -rp command is used to copy directories and their contents from one location to another while preserving their permissions and ownership

### sed command:
Used for text manipulation, primarily used for searching and replacing text within a file or stream of text.

#### syntax:
```
sed [options] 'command' file
```
### date command:
Used to display current date/time.

#### syntax:
```
date +"%Y-%m-%d %H:%M:%S"
```
```
sudo date --set="2022-05-01 12:00:00"
```

### find command:
Used to find/ search files.

#### syntax:
```
find . //find all files in dir
```
```
find . -name "*.txt"
```

### grep command:
used to search through the file ,looking for matches to the pattern specified.

#### example:
```
grep "pattern" file.txt
```
```
grep "pattern" file1.txt file2.txt
```
```
grep -r "pattern" . // recursive search in all sub dirs
```
```
grep -i "pattern" file.txt // case insensitive
```

### du command:
show disk usage space.

#### example:
```
du file.txt //To display the disk usage of a file
```
```
du -h directory/
```
```
du -h --max-depth=1 //To display the disk usage of all subdirectories
```
### df command:
show disk free space.

#### example:
```
df -h /dev/sda1 //To display disk usage information for a specific file system in human readable
```
### diff command:
show difference between files.
#### example:
```
diff file1.txt file2.txt
```
```
diff -u file1.txt file2.txt > changes.patch
```
```
patch file.txt < changes.patch
```
### wc command:
To find number of lines, word count, characters count byte in the file.

#### example:
```
wc -l file.txt //To count the number of lines in a file
```
```
wc -w file.txt //To count the number of words in a file
```
```
wc -c file.txt //To count the number of characters in a file
```
### tar command:
To saving several files into an archive.

#### example:
```
tar -cvf archive.tar file1.txt file2.txt directory/
```
- create a new tar archive file called archive.tar that contains file1.txt, file2.txt, and directory/. The -c option specifies that a new archive should be created, -v specifies verbose mode to display the progress of the operation, and -f specifies the name of the archive file.
```
tar -xvf archive.tar //extract
```
```
tar -rvf archive.tar newfile.txt //To append files to an existing tar archive file
```
```
tar -tvf archive.tar //list
```
### zip command:
Used to compress and archive data.

#### example:
```
zip archive.zip file1.txt file2.txt directory/
```
- This will create a new ZIP archive file called archive.zip that contains file1.txt, file2.txt, and directory/.
```
unzip archive.zip
```
```
zip archive.zip newfile.txt // add
```
```
unzip -l archive.zip // list
```
### ln command:
 Used to create links between files or directories.

#### example:
```
ln file1.txt link1.txt
```
- create a hard link called link1.txt that points to the same data as file1.txt. If you modify either file1.txt or link1.txt, the changes will be reflected in both files.
```
ln -s /path/to/file1.txt link2.txt
```
- Unlike a hard link, a symbolic link points to the path of the original file rather than the physical data. file is deleted, the symbolic link will be broken and will no longer work. If you modify either file1.txt or link2.txt, the changes will be reflected in both files.

## User management:

### useradd command:
To add new user.
#### example:
```
sudo useradd username
```
### userdel command:
To remove user.

#### example:
```
sudo userdel username
```
```
sudo userdel -f username
```
```
sudo userdel -r username
```
- To delete the home directory and all files owned by the user, you can use the -r option.

### passwd command:
To change the user account passwords.

#### example:
```
passwd user1
```
```
passwd -e username //To force a user to change their password the next time they log in
```
```
passwd -l username //Locking(-l) and(-u) unlocking a user's password
```

## Access management:

### ssh command:
To access remote server.

#### syntax:
```
ssh username@remote_host "command"
```
- executes command in server.

### scp command:

```
scp file username@remote_host:/path/to/destination
```
- Replace file with the path to the file you want to copy, username and remote_host with the appropriate values, and /path/to/destination with the path to the destination directory on the remote machine.

### sudo command:
To give permission to the user same as admin.

#### example:
```
sudo apt-get update
```
```
sudo apt-get upgrade
```
### su command:
switch current user to another user.

#### example:
```
su username
```
### chmod command:
To give permissions to files or directories.

#### example:
```
chmod [options] [u|g|o|a][+|-|=][r|w|x] file(s)
```
- The u option represents the owner, g represents the group, o represents other users, and a represents all users. The + symbol adds the permission, - removes the permission, and = sets the permission. The r option represents read permission, w represents write permission, and x represents execute permission.

- to add read and write permission for the owner and group of a file, you can use the following command
```
chmod ug+rw file.txt
```

### chown command:
 to change the file Owner or group.

#### example:
```
chown owner_name file_name
```
```
chown root file1.txt
```

## Configuration management:

### env command:
used to display your current environment or run a specified command in a changed environment.

#### example:
```
env
```
```
env VAR=value command
```
- env command to set environment variables for a command or a process.
```
env -u VAR command
```
- env command to unset environment variables.

### echo $PATH command:
used to display the path of the url

#### example:
```
echo $PATH
```
```
export PATH=$PATH:/path/to/new/directory
```
- This will append the directory /path/to/new/directory to the existing PATH variable.

### export command:
When you use the export command, you're telling the shell to pass the variable and its value to any child processes or commands that are executed from the shell.

#### example:
```
export VAR=value
```
```
export PATH=$PATH:/path/to/new/directory
```
- This will append the directory /path/to/new/directory to the existing PATH variable.

### hostname command:
Used to display machine hostname.

#### example:
```
hostname
```
### netstat command:
Display connection information.

#### example:
```
netstat
```
### crontab command:
the crontab command is used to schedule and manage cron jobs. A cron job is a command or script that is scheduled to run automatically at specified intervals.
#### example:
```
crontab [options] file
```
- The options are used to specify various options for the crontab command, such as -e to edit an existing cron job or -l to list all cron jobs.

### kill command:
used to stop running process.
#### example:
```
kill -l
```
- dispaly a list of kill commands that you run regular.

```
kill [signal] PID
```
-  signal to be sent to the process, and "PID" is the process ID of the process to be terminated. The default signal sent is SIGTERM (15), which instructs the process to terminate gracefully.

- If the process is still running after sending the SIGTERM signal, a stronger signal like SIGKILL (9) can be sent to force the process to terminate immediately.

```
kill -9 PID
```

### pkill command:
The "pkill" command is similar to the "kill" command, but instead of using a process ID (PID), it searches for processes based on their name or other attributes.
#### example:
```
pkill [options] pattern
```

```
pkill -f myapp
```

### curl command:
Used to transfer data to or from a server, using various protocols such as HTTP, FTP, SMTP, etc. It can be used to download or upload files, test APIs, and perform various other network-related tasks.

#### example:
```
curl [options] [URL]
```
- Where "URL" is the URL of the resource to be transferred, and "options" are various options that can be used to customize the behavior of the command.

- The "-o" option tells "curl" to write the output to a file instead of the console.

```
curl -o localfile.txt http://example.com/remotefile.txt
```
- Other options include "-u" to specify a username and password for authentication, "-X" to specify the HTTP method to be used (e.g., GET, POST, PUT, DELETE), and "-H" to specify HTTP headers to be sent with the request.

- Curl" can also be used to send data to a server, for example, to submit a form or test an API endpoint. The following command will send a POST request with some data to a remote server,
```
curl -X POST -d "name=John&age=30" http://example.com/api/endpoint
```
- The "-d" option specifies the data to be sent with the request in the format "key=value".

### ping command:
used to know our machine is able comminicate or not with server.

#### example:
```
ping google.com
```

### wget command:
used to download files from the internet or intranet using various protocols such as HTTP, FTP, and HTTPS. It can be used to download individual files, recursively download entire websites, and perform various other file retrieval tasks.
#### example:
```
wget [options] [URL]
```

```
wget http://example.com/remotefile.txt -O localfile.txt
```
- The "-O" option tells "wget" to write the output to a file instead of the console.

- Other options include "-c" to resume a partially downloaded file, "-r" to download recursively, "-np" to prevent downloading files from parent directories, and "-U" to specify a user agent string.

```
wget --mirror --convert-links --no-parent http://example.com/
```
- The "--mirror" option tells "wget" to download recursively and create a mirror of the website, "--convert-links" tells "wget" to convert links to point to the local files, and "--no-parent" tells "wget" to not download files from parent directories.

### history command:
To display all used commands.
#### example:
```
history
```
### uname command:
Displays the information about the system.
#### example:
```
Uname
```
### ps ux command:
used to display information about running processes on a system. It shows a detailed list of all processes running under the current user account, including their process ID (PID), CPU usage, memory usage, start time, and other information.
#### example:
```
ps ux
```
- When run, the "ps ux" command will display a list of all processes running on the system, including the following information for each process:

USER: The username of the user who owns the process
PID: The process ID of the process
%CPU: The percentage of CPU usage by the process
%MEM: The percentage of memory usage by the process
VSZ: The virtual memory size of the process in kilobytes
RSS: The resident set size (i.e., non-swapped physical memory) of the process in kilobytes
TTY: The controlling terminal of the process (if any)
STAT: The current status of the process (e.g., running, sleeping, stopped, zombie, etc.)
START: The start time of the process
TIME: The total CPU time used by the process
COMMAND: The command-line used to start the process.

- "-ef" option is used to display all processes in a full format.

## log management:

### syslog command:
To manage system messages and events. It allows system administrators to centralize system log files and track system events, errors, and warnings across multiple systems.

- where a client process running on a system generates log messages and sends them to a central syslog server. The syslog server receives and stores the messages in a centralized log file or database, where they can be analyzed and monitored by system administrators.

- Syslog can be configured using the "rsyslog" or "syslog-ng" daemons, which are widely used in modern Linux distributions. These daemons allow system administrators to customize the logging behavior of the system, filter and forward logs to different destinations, and set up alerts and notifications based on log events.

### journalctl command:
used to query and view system logs collected by the systemd journal service on Linux systems. The systemd journal is a system logging service that captures log messages from various sources, including kernel messages, system services, and user applications.

#### Some of the most commonly used options for the "journalctl" command include:

- "-u" for Display logs for a specific systemd unit (e.g., "-u apache2" to display logs for the Apache web server).
- "-f" for Follow the log output in real-time (similar to "tail -f").
- "-n" for Show the last N log entries (e.g., "-n 100" to display the last 100 log entries).
- "--since" to Display logs since a specific date or time (e.g., "--since '2022-01-01 00:00:00'" to display logs since January 1st, 2022 at midnight).
- "--until" to Display logs until a specific date or time (e.g., "--until '2022-01-01 00:00:00'" to display logs until January 1st, 2022 at midnight).
- "--grep" to Search for a specific string or regular expression in the log messages (e.g., "--grep 'error'").


- The "journalctl" command also supports output formatting options, such as displaying logs in a more human-readable format using the "--output=verbose" option, or exporting logs to a file using the "--output=json" option.

### custom logs:
The "journalctl" command also supports output formatting options, such as displaying logs in a more human-readable format using the "--output=verbose" option, or exporting logs to a file using the "--output=json" option.

## Network management:

### ifconfig command:
 "ifconfig" command displays a list of all active network interfaces on the system, along with their configuration details such as IP address, netmask, MAC address, and other network-related settings.

 #### output:
 eth0      Link encap:Ethernet  HWaddr 00:11:22:33:44:55
          inet addr:192.168.1.100  Bcast:192.168.1.255  Mask:255.255.255.0
          inet6 addr: fe80::211:22ff:fe33:4455/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:1234567 errors:0 dropped:0 overruns:0 frame:0
          TX packets:9876543 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:1234567890 (1.23 GB)  TX bytes:9876543210 (9.87 GB)

### http vs https:
- http - http stands for a hypertext transfer protocol used for transferring data over a network , includes website content and API calls ,uses http protocol. There are two main kinds of http messages: request and responses.

- https -The S in https stands for secure. Https uses TLS(SSL) to encrypt normal http requests and responses.As a result ,https is far more secure than http.

### internal network:
- An internal network, called an intranet, is one which is restricted to a defined set of users. An example would be a network accessed only by the employees of a specific company.

### external network:
- An external network (e.g., the Internet) allows users of all types access. Besides the Internet, an example would include a network that allows customers to connect to company to place orders.

### TCP:
TCP means transmission control protocol ,TCP provides reliable, ordered, and error-checked delivery of data  through a connection based protocol while tcp is more reliable,it transfers data more slowly.

### UDP:
UDP means user datagram protocol ,is a connectionless. UDP is less reliable but works more quickly.

### Private subnets:
A private subnet, on the other hand, is a subnet that does not have a route to the Internet Gateway.

### Public subnets:
A public subnet is a subnet that has a route to the Internet Gateway.

### CIDR range:
(Classless Inter-Domain Routing) is a method of IP address allocation that allows for more efficient use of the available IP address space. CIDR range calculations are used to determine the network and host portions of an IP address and subnet mask pair, and to calculate the range of IP addresses that belong to a particular network.


#### example:
255.255. 255.0 (in dotted decimal notation) has 24 leading 1 bits, so its CIDR prefix is /24.

### ports:
To identify a specific process to which an internet or other network message is to be forwarded when it arrives at a server.

#### example:
Ports 20 and 21: File Transfer Protocol (FTP). ... Port 22: Secure Shell (SSH). ... Port 25: Historically, Simple Mail Transfer Protocol (SMTP). ... Port 53: Domain Name System (DNS). ... Port 80: Hypertext Transfer Protocol (HTTP). ... Port 123: Network Time Protocol (NTP).

## Application / web servers:

### Application server:
An application server is a software framework that provides an environment in which applications can be deployed, run, and managed. It typically includes features such as security, scalability, load balancing, and resource management. Application servers are used to host and run web applications, enterprise applications, and mobile applications. Examples of popular application servers include Apache Tomcat, IBM WebSphere, Oracle WebLogic, and JBoss. Application server can also have its own web server.

#### example case(cant find data):
- it accepts server let requests from web server(sends through interface in system that connects to app server) as web server cant find response in its static DB. it checks in its own database and sends server let response which web server will send http response to client.

### web server:
A web server, on the other hand, is a software program that runs on a computer and is responsible for serving web pages to clients over the internet or an intranet. It listens for incoming requests from clients and responds with the requested content, typically in the form of HTML pages, images, and other static or dynamic content. Examples of popular web servers include Apache HTTP Server, Microsoft IIS, Nginx, and Google Web Server.

## load balancing:
A load balancer is a network device or software program that helps distribute incoming network traffic across multiple servers or resources. Its primary purpose is to ensure that all the resources available to a network or application are being used effectively, and that no single server is overwhelmed with too much traffic. Load balancers can be hardware devices or software programs, and they work by monitoring the traffic coming into a network and intelligently distributing it across multiple servers.

Load balancers can be used to improve the performance, reliability, and availability of web applications, enterprise applications, and other network services. By distributing traffic across multiple servers, load balancers can help prevent downtime caused by server failures, reduce the risk of overload, and improve the overall performance of the network.

There are several different types of load balancers, including Layer 4 (Transport Layer) load balancers, which operate at the network layer and distribute traffic based on IP address and port number; Layer 7 (Application Layer) load balancers, which operate at the application layer and distribute traffic based on the content of the requests; and Global Server Load Balancers, which can distribute traffic across multiple data centers or regions. Some popular load balancing solutions include NGINX, Apache Traffic Server, F5 BIG-IP, and Amazon Elastic Load Balancer (ELB).

## High availability:
High availability refers to the ability of a system or application to remain operational and accessible to users for a specified period of time, typically measured in terms of uptime percentage. High availability is achieved through a combination of hardware, software, and networking technologies that help ensure that a system or application can continue to function in the event of hardware or software failures, network outages, or other disruptions.

##### Methodoligies to achieve HA:
- #### Redundancy: 
This involves duplicating critical components of the network, such as switches, routers, or servers, so that if one fails, another can take over without interruption to service.
- #### Load balancing:
This involves distributing traffic across multiple servers or paths to prevent any single server or path from becoming overloaded or unavailable.
- #### Failover:
This involves automatically switching to a backup or secondary system in the event of a failure or outage. For example, if a primary server fails, a secondary server can automatically take over to ensure continuity of service.
- #### Network virtulisation:
This involves creating virtual instances of network devices or services, which can be moved or migrated between physical devices as needed to ensure continuous service.


## Create shell script to install Application servers and proxy tools:

```
#!/usr/bin/bash 
#Install Java Development Kit (JDK)
sudo apt-get update
sudo apt-get install -y default-jdk

#Install apache tomcat server
nano install_tomcat.sh

#install_tomcat.sh (with version as argument) file content:

#req_tom_ver="9.0.74"
req_tom_ver=$l
tom_m_v=$(echo $req_tom_ver | cut -c l)
url = "https://dlcdn.apache.org/tomcat/tomcat-$(tom_m_v)/v$(req_tom_ver)/bin/apache-tomcat-$(req_tom_ver).tar.gz"
wget $url
tar -xvzf apache-tomcat-${req_tom_ver}.tar.gz 
mv apache-tomcat-${req_tom_ver} tomcat${tom_m_v} 
rm -rf apache-tomcat-${req_tom_ver}.tar.gz

./install_tomcat.sh 9.0.74

#conf file contains logging props(set logging path) server.xml contain start and shutdown port.
#tomcat-users.xml we insert roles for users to access gui. catalina.properties for jar related configurations.
cd /tmp/
wget https://your git repo/master/tomcat-users.xml //add your modified file(added roles with username and password) from git
wget https://your git repo/master/context.xml //add your modified file from git
cp tomcat-users.xml /opt/tomcat/conf/tomcat-users.xml
cp context.xml /opt/tomcat/webapps/manager/META-INF/

nano startup.sh // we can set paths of env variables or (cat /etc/systemd/system/tomcat.service) set paths

systemctl daemon-reload
sh startup.sh (or) systemctl start tomcat
systemctl enable tomcat
echo "Done"

#Install ha proxy server
sudo apt install haproxy -y	
```
## configure proxy to access application server through proxy:
```
sudo bash -c 'nano /etc/haproxy/haproxy.cfg' (or try) 'cat << EOF >> /etc/squid/squid.conf'

# many sections will be available, global section defines security, performance tunings that effect ha proxy at low level.
# default section have configurations that are applied to frontend(defines ips and ports) and backend(web server that handles requests). we can define multiple default sections, but first is taken into effect.
front and backend can be combined through listen section.

# configure global section by adding:
tune.ssl.default-dh-param 2048
# this line is used to set maximum size of diffie hellman parameters which is used for generating the temporary hellman key in case of the key exchange.

# add sections with names (after defaults sec):
frontend sec_name
stats url /haproxy?stats
bind 192.168.1.16:443(load balancer ip) ssl crt /etc/ssl/certs/haproxy.pem 
default_backend (name of backend section)


backend sec_name
balance roundrobin 
server hostname 192.168.1.14:80(your server ip) check 
server hostname 192.168.1.15:80(your server2 ip) check
listen stats
  bind 192.168.1.16:443(load balancer ip) ssl crt /etc/ssl/certs/haproxy.pem 
  stats enable                # enable statistics reports
  stats hide-version          # Hide the version of HAProxy
  stats refresh 30s           # HAProxy refresh time
  stats show-node             # Shows the hostname of the node
  stats auth admin:P@ssword   # Authentication for Stats page
  stats uri /lb_stats         # Statistics URL

// quit nano

#next how to configure HA proxy with ssl, for this we need to generate ssl certificate for ha proxy.
openssl genrsa -out /etc/ssl/private/haproxy.key 2048

//generates private key, next generate certificte sign request
openssl req -new -key /etc/ssl/private/haproxy.key -out /etc/ssl/certs/haproxy.csr

//give details, csr gets generated. next we create signed certificate
openssl x509  -req -days 365 -in /etc/ssl/certs/haproxy.csr -signkey /etc/ssl/private/haproxy.key -out /etc/ssl/certs/haproxy.crt

//now certificate is created, now we can create ssl pem file with both key and certificate.
cat /etc/ssl/private/haproxy.key /etc/ssl/certs/haproxy.crt >> /etc/ssl/certs/haproxy.pem

//ssl conf for HA proxy completed.
haproxy -c -f /etc/haproxy/haproxy.cfg

sudo systemctl restart haproxy
```
- check in browser serverip/haproxy?stats


























