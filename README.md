high-level approach:
I generally followed what was sugguested on the homework instructiosn. First I started by writing a
program that could successfully take in the command line input. Then I implemented string parsing to
get the username, password, and any file directories out of the command line input.

Afterwards, I worked on the connection establishment. I created support for connecting and logging
into the server. This included successfully sending USER, PASS, TYPE, MODE, STRU,and QUIT commands.

Then, I worked on the directory commands and the remove commmand. These were pretty straight 
forward as I just had to send the correct command to the control channel. There was no need to 
establish a data channel.

Penultimately I worked on the PASV and List commands. Here I had to create a second socket to
read and write data to the FTP server and my local machine. The LIST command was simiar to the 
previous commands where I just had to send the command to successfully implement the ls command.

Lastly, I worked on STORE, RETR, and DELE. This included using the second socket, data channel,
that I created to utilize list. These commants were essential to implement the copy and move commands.
First, I worked on the copy command. Which included reading/writing files to a local server and also
reading/writing files to an FTP.

any challenges you faced:
A challenge that I initally faced was just a conceptual high level understanding of what the project
wanted. However, once I went to office hours and fully understood the format, the project
was more straightforward. 

Another big problem that I faced was just the general unfamiliarity with python. A majority
of my time was spent looking through documentation as opposed to coding. I expect this 
challenge to be less of an issue in future projects.

overview of how you tested your code:

Testing of my code mainly consisted of logging on to the FTP client and looking at what files 
successfully were added/removed/moved. I would run commands then check WinSCP to see if they
did what they were intended to do.

Additonally, I printed out all of the output from both the control channel and the data channel.
This helped testing as the codes accociated with the output could help me debug my code.
