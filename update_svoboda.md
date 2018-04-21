**UPDATING STAFF PAGES & JMS DIARY DATA:**

**1. Editing the Staff Pages**
Link to Staff Pages: http://depts.washington.edu/newbook/staff

*Machine names:* [name].u.washington.edu (This is for FileZilla or Cyberduck) Port: ##
Website located in the folder **public_html**

*If using ssh or sftp to open a connection*, need to use [account]@[name].u.washington.edu
From Homer Main Menu (opening screen), select **S** to open the shell
[to create a new file, etc. see detailed file: **edit_staffpages**]
**2. Editing and Updating JMS Diaries Data**

**--> Change Link Page Information**
OPEN terminal window
LOG IN ssh [account]@[name].u.washington.edu
CHANGE directory to cd public_html/data/JMS
EDIT jms_idx.html
BACK UP existing file cp jms_idx.html jms_idx_YYYYMMDD.html
EDIT nano/pico jms_idx.html
GO to location of the diary to be updated -- #d38/d38
CHANGE old Diary_38_20180309lb.html to new name/date (4x)
Change the name to the current diary file: http://depts.washington.edu/newbook/data/JMS/jms_idx.html

**--> Receiving Data from Diary Leads**
OPEN GMAIL to view message with linked data
SAVE the matched diary txt and xml files to the DOWNLOADS folder
MOVE the txt and xml files to d# folder on the local Desktop


**--> Update Diary Data**
OPEN terminal and LOGIN (above)
CHANGE directory to d## (ex. d38) — public_html/data/JMS/d##
RUN sh bak_rem.sh -- (script copies data to "old" and deletes generated files)
UPLOAD new diary data files (txt and xml); can use: sftp newbook@homer.u.washington.edu, Cyberduck, Filezilla
BACK UP existing file cp jms38_mak.sh jms38_mak_20180309.sh
EDIT jms38_mak.sh
CHANGE old Diary_38_20180309lb.html to new name/date
UPLOAD new diary data from local Desktop folder (sftp,Cyberduck,FileZilla)
RUN sh jms38_mak.sh -- (script generates html and tex files)
UPDATE wordlists, run sh wordlist_d37.sh


**--> Generate PDF file**
LOGIN to ovid, ssh ovid
CHANGE directory to d## (ex. d38) — public_html/data/JMS/d##
RUN pdflatex d##_MMDD.tex -- do this twice

**--> Creating Directory for New Diary**

mkdir d##
cd d##
cp ../d38/* .
Rename to match new diary ##


--------------------------------------------------------------------------------------------
Revised 03/28/2018
Revised 04/04/2018
Revised 04/11/2018
