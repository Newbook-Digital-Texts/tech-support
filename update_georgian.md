**UPDATING GEORGIAN DATA**

**--> Receiving Data from Transcribers**
Download transcriptions from Google Drive and
save them to GitHub?

**--> Validating HTML**

**--> Put Transcriptions On Server**
**--> Put Transcriptions On GitHub ??**
**FIRST...**
LOGIN to server: ssh [account]@[name].u.washington.edu
SELECT **S** for Shell in the Homer Menu

**--> Convert from HTML to XML**
ENTER source virtenv/bin/activate
GO TO cd GDTC_site
GO TO support folder: cd gdtc_support
GO TO new folder: cd new_folder ( ls -al to view transcriptions)
RUN python3 xmlParser1.8.py
