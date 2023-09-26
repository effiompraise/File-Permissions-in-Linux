# File-Permissions-in-Linux
As a cybersecurity analyst, I have been tasked to examine existing permissions on the file system. This means that I need to determine if the permissions match the authorization that should be given. If they do not match, I’ll need to modify the permissions to authorize the appropriate users and remove any unauthorized access.

# Checked file and directory details
<p>The command I used to check file and directory details is: ls -al</p>
<img src="https://imgur.com/XLVQBmC.png" height="80%" width="80%" alt="File and directory details"/>

# Permissions String Described
<p>In the /home/researcher2/projects directory, there are five files with the following
names and permissions:
</p><br\>

● project_k.txt
○ User = read, write,
○ Group = read, write
○ Other = read, write

● project_m.txt
○ User = read, write
○ Group = read
○ Other = none

● project_r.txt
○ User= read, write
○ Group = read, write
○ Other = read

● project_t.txt
○ User = read, write
○ Group = read, write
○ Other = read

● .project_x.txt
○ User = read, write
○ Group = write
○ Other = none

<p>There is also one subdirectory inside the projects directory named drafts. The
permissions on drafts are:
</p>

● User = read, write, execute

● Group = execute

<p>To explain the drafts subdirectory: drwx--x---</p>
<p>It means this is a directory because of the “d” right before “rwx”. The read and write permissions are only available to users, while executable permission is only available to users and groups. Other has no permissions.</p>

# Changed file permission
<p>Project_k.txt currently has write permission and since my organization doesn’t allow other to have write access to any files, I’ll be removing access.</p>

<p>From the /home/researcher2/projects/ directory to display the list of files I used the command ls -l and to remove the write permission on other I used the command chmod o-w project_k.txt</p>
<img src="https://imgur.com/NqtfUMM.png" height="80%" width="80%" alt="Changing file permission"/>

# Changed file permission on a hidden file
<p>To assign proper authorization for the hidden file project_x.txt I used the command chmod u-w,g-w,g+r .project_x.txt</p>
<img src="https://imgur.com/jcMHLKE.png" height="80%" width="80%" alt="Assigned proper authorization"/>

# Changed directory permissions
<p>I used the command chmod g-x drafts give only the user (researcher2) access to the drafts directory contents.</p>
<img src="https://imgur.com/bAEvEH5.png" height="80%" width="80%" alt="Changed directory permissions"/>

# Summary
<p>I reviewed and modified permissions to authorize the appropriate users and remove any unauthorized access to files and directories using the Linux command line. I changed the permission to certain owners and ensured unauthorized access was reviewed and corrected.</p>


