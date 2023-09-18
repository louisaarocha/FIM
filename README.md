# File Integrity Monitor using Powershell 
---------

## Project Summary 
This project emphasizes the importance of integrity in cybersecurity by demonstrating a basic file integrity monitor that will monitor files and have the ability to raise alerts when changes have occured to the files. 

## Project Steps

1. **FIM Folder**
   - Created folder on ‘Desktop’ named ‘FIM’.
   - This folder contains the FIM PowerShell script, text files that are being monitored, and the baseline text file. 

2. **User input** 
   - Implemented code for user input. 
   - The user will have the option to either A) collect a new baseline or B) begin monitoring files saved in the baseline.
   - Using if-else statements, implemented the logic for option A and option B.  
<br>
<p align="center">  
   <img src="https://imgur.com/PvyOmwN.png" height="60%" width="60%" alt="Alt text" title="User input">
</p>
<br>

3. **Calculate hash for files**
   - Created a function that calculates the hash for the file paths.
     
<br>
<p align="center">  
   <img src="https://imgur.com/6ebdykg.png" height="60%" width="60%" alt="Alt text" title="Calculate hash function">
</p>
<br>

4. **Delete baseline if it already exists**
   - Created a function that will delete the baseline file if it already exists.
  
<br>
<p align="center">  
   <img src="https://imgur.com/1g7xg4A.png" height="60%" width="60%" alt="Alt text" title="Delete function">
</p>
<br>

5. **Option A logic:** 
   - Note: The goal for option A is to collect all the files in our directory that we want to monitor. We have a folder called ‘FIM’ that contains our FIM script and the files we want to monitor. We want to look inside this folder, collect all the hashes from these files, and then store them in a text file that will contain the hash and the file path for each file, which will be our baseline.txt file.
   - Created a variable that will collect all the files from the target folder.
   - Created for loop that will loop through the files folder and create a hash for each file and store it into the baseline.txt.
   - Tested script by adding new files into the folder. 
     
<br>
<p align="center">  
   <img src="https://imgur.com/M7mpk2W.png" height="60%" width="60%" alt="Alt text" title="Collect files from folder test">
</p>
<p align="center">  
   <img src="https://imgur.com/tc8DWWw.png" height="60%" width="60%" alt="Alt text" title="Loop test">
</p>
<br>

6. **Option B logic:**
   - Note: The goal for option B is to monitor the files in the baseline and alert the user when changes are made. This will be done by creating an empty dictionary that will be used to load the files from baseline.txt and store them in the dictionary. By adding a Start-Sleep command, will check our files every 2 seconds to monitor changes. Whether a file has been deleted, changed, or a new file has been created.
   - Created an empty dictionary that will collect and store the path and hash for each file into the new dictionary.
   - Began continuously monitoring files in the saved baseline for changes.
   - Start-Sleep command will check files every 2 seconds for changes. 
   - Notify the user if a new file has been created, changed, or deleted. 

<br>
<p align="center">  
   <img src="https://imgur.com/efu6FQ9.png" height="60%" width="60%" alt="Alt text" title="Dict test">
</p>

<p align="center">  
   <img src="https://imgur.com/JP2Z7tL.png" height="60%" width="60%" alt="Alt text" title="New file created">
</p>

<p align="center">  
   <img src="https://imgur.com/KLBBZQg.png" height="60%" width="60%" alt="Alt text" title="Before file alteration">
</p>

<p align="center">  
   <img src="https://imgur.com/xdtSJKs.png" height="60%" width="60%" alt="Alt text" title="After file alteration">
</p>

<p align="center">  
   <img src="https://imgur.com/FZKKIH1.png" height="60%" width="60%" alt="Alt text" title="Deleted file">
</p>
<br>

7. **Finished FIM**
<br>
<p align="center">  
   <img src="https://imgur.com/Z8f5pJ9.png" height="60%" width="60%" alt="Alt text" title="FIM">
</p>
<br>


















## Languages Used
   - PowerShell
  
<br>

