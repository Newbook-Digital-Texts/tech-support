**UPDATING GEORGIAN DATA**
- Process for converting XML data to HTML

**Receiving Data from Transcribers**
- Download transcriptions from Google Drive and add them
to Server folder: [FOLDER NAME]

**Validating HTML**

**Put Transcriptions On Server**
- Can use Cyberduck,FileZilla
- LOGIN to server (through one of the programs above)
-
**Put Transcriptions On GitHub (needs to be edited)**
- LOGIN to server
- SELECT **S** for Shell in Menu
- cd [FOLDER NAME]
- git add .
- git commit -m "Add new transcriptions"
- git push

**Convert from XML to HTML and PHP files**
- OPEN the terminal
- LOGIN to the server
- CHANGE DIRECTORY to access virtual environment: cd public_html/mcb
- ACTIVATE virtual environment: source virtenv/bin/activate

*virtualenv (allows one to access python libraries to run parser script that may or may not be on the server version - dependencies are consistent - using virtenv's verion of python)*

- CHANGE DIRECTORY to access parser script:
  - cd public_html/mcb/GDTC_site/gdtc_support/new_folder

- ADD new transcriptions to xml folder (in same directory):
  - can use sftp, FileZilla, Cyberduck, etc.

- RUN xml parser script: python3 [script-name]
