# Connection Scripts

Connect_SSH and Connect_SFTP scripts save you from retyping connection string
and remembering your server's IP address. 

## Create a Connection Key

Use SSH keys to connect to your production server, they are more secure than 
passwords.

From your home directory, create a new SSH key for you upcoming production server by:

`ssh-keygen -t rsa`

As a  file name, enter .ssh/server-url, for example, .ssh/code.linedrop.io

Keep the password empty.

To view all your ssh keys, run:

`ls ~/.ssh`

## Connect_SSH 

Open the script in a text editor and change key_file to the name of your 
ssh key file, user to your user name, and server_ip to your server IP address.  For example,

ssh -i ~/.ssh/code.LineDrop.io paul@127.0.0.1

To run the script, specify the directory:

`./connect_ssh`

## Connect_SFTP

Server SFTP connection script makes the process of creating an SFTP to the server simple.  

Open the script in a text editor and change key_file to the name of your 
ssh key file, user to your user name, and server_ip to your server IP address.  For example,

sftp -i ~/.ssh/code.LineDrop.io paul@127.0.0.1

To run the script, specify the directory:

`./connect_sftp`

## Uploading 

To upload files to the server, using the Terminal browse to the directory 
with the files to be uploaded start an SFTP connection.

`./connect_sftp`

Upload each file using _put_ command and specifying the name of the file:

`put myfile`


