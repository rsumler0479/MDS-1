# MDS

https://developers.google.com/docs/api/samples/mail-merge  ( lINK FOR THE SAMPLE CODE )
https://developers.google.com/docs/api/quickstart/python   ( LINK FOR PYTHON & GOOGLE API INTEGRATION )
https://github.com/googleworkspace/python-samples/tree/master/docs/mail-merge ( GITHUB LINK FOR SAMPLE CODE )
https://docs.google.com/document/d/1HFO_F_10d0VpCUFXaoR4ZOr6gLoLN0ST/edit?usp=sharing&ouid=100095792606716249357&rtpof=true&sd=true  ( LINK TO GOOGLE SHEET )



-
IMRPOVING THE CODE PLAN 
1. SOLVE ERRORS
2. FORMULATE CODE FOR OUR PURPOSE
3. GET CODE TO MEMORTIZE YOUR CREDINTIALS ( CODE FOUND ONLINE BELOW ) 

PyDrive code that automate google drive api authetication. Use the browser just one time to authenticate and never more. It saves your credential data on mycreds.json :)

from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive

gauth = GoogleAuth()
gauth.LoadCredentialsFile("mycreds.json")

if gauth.credentials is None:
    gauth.LocalWebserverAuth()

elif gauth.access_token_expired:
    gauth.Refresh()

else:
    gauth.Authorize()

gauth.SaveCredentialsFile("mycreds.json")

4. GET CODE TO DOWNLOAD TEMPLATE AS PDF AFTER MERGING 
