# FTP

_#unix_ _#bash_ _#file-sharing_

```bash
# Start FTP client
$ ftp

# Connect to FTP server
ftp> open <ip> <port>
Name: <username>
Password: <password>

# List remote directory's files and folders
ftp> ls

# Change working directory on remote host
ftp> cd <directory>

# Show current directory on remote host
ftp> pwd

# Toggle interactive mode
ftp> prompt

# Run command on local machine
ftp> ! <command>

# Set file transfer type to binary
ftp> binary

# Download multiple files (prefix_foo.txt, prefix_bar.jpg, ...)
ftp> mget <prefix>*

# End FTP session and exit FTP client
ftp> bye
```
