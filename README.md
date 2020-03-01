# Environment Variables Lab

## Timings

45 - 60 Minutes

## Summary

We know how to set environment variables and how to persist them between logins by adding them to the bashrc file.

But we're using Vagrant to automatically create environments and we don't want the developers to have to do this manually.

We need to use an environment variable to tell the app the location of the database running on the db VM.

```
mongodb://192.168.10.150:27017/posts
```
## my personal notes :
app.js is where it happens

DB_HOST = mongodb://192.168.10.150:27017/posts
export $DB_HOST
npm install --no-bins-links # this prevents npm creating symlinks for any binaries the package may contain
npm start <- to set up port
 symbolic link, also termed a soft link, is a special kind of file that points to another file, much like a shortcut in Windows or a Macintosh alias. Unlike a hard link, a symbolic link does not contain the data in the target file.

 app.js      -       app vm to connect to db vm

 provision1:
 vagrant up
 user: Vagrant

provision:2
 vagrant ssh app          
 user: Vagrant
 cd/home/ubuntu/app
 npm install --no-bins-links      <--- another child process
 it sesrches through and make it starts. put data into database and looking for it. database connecting

 npm start

 you will see 'database cleared' and 'database seeded'

 ------
 exports make it visible to other programs, and not locally
 echo - makes it print

 ---
 use sudo to do as admin rights
 root is the highest permission rights
dont need to do sudo as we are using Vagrant

_____

## Tasks

* Write a bash command that will inject an export line in to the bashrc
* Use Vagrant a shell provisioner to run this command
* Use your script to create an environment variable called DB_HOST with the correct value for connecting to the database
* Start the app and ensure that the /posts route is now connected correctly

## Bonus

Use ruby to create a method that allows you to easily add more environment variables in the future as needed.

## Tips

the HEREDOC syntax in ruby is a useful way to create big blocks of code as strings.


add another line
test 2



typing this sentence to test, please ignore. 

