This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or  (at your option) any later version.This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. You should have received a copy of the GNU General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>.

![Objects](https://www.linux-toys.com/object33.png)



[How to run the program]

To run the application, most users should be able to run the program by double clicking on the CloudExplorer.jar file. If not, there are two scripts included to assist:

Linux and OS X users can run it as follows:
./cloudExplorer

Windows users can run Cloud Explorer by double clicking on the cloudExplorer.bat or CloudExplorer.jar file.

For any OS, you can start the program with the Java command:

java -jar -Xms100m -Xmx500m ./CloudExplorer.jar


[How to migrate data between S3 accounts]

Load the destination account and click "Set as migration Account" under Settings.
Create the destination bucket on the destination account.
Load the origin S3 account and select the bucket to transfer to the new S3 account.
Under the "Tools" menu, select "Migrate bucket to another S3 account".
Type in the destination bucket name and click "Start Bucket Migration".
Wait for transfers to complete.


[Background Sync]

Background Sync allows Cloud Explorer to function like Dropbox. It will sync to and from the S3 server. Please note that no files will be deleted. 
<br>
<br>
From the GUI: 
<br>
Click on "Background Syncing"
<br>
Click Configure
<br>
Click on a destination Directory
<br>
Click Save.
<br>
Click on "Background Syncing"
<br>
Click "Run".
<br>
Syncing will occur every 5 minutes.

<br>
Starting background sync from the Command Line (Useful for running as a background process):

Create your config file from the GUI.
<br>
$ java -jar -Xms100m -Xmx500m CloudExplorer.jar daemon
