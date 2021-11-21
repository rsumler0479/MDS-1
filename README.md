# MDS

https://developers.google.com/docs/api/samples/mail-merge  ( lINK FOR THE SAMPLE CODE )
https://developers.google.com/docs/api/quickstart/python   ( LINK FOR PYTHON & GOOGLE API INTEGRATION )
https://github.com/googleworkspace/python-samples/tree/master/docs/mail-merge ( GITHUB LINK FOR SAMPLE CODE )
----------
IMRPOVING THE CODE PLAN 
1. SOLVE ERRORS
2. GET CODE TO MEMORTIZE YOUR CREDINTIALS ( CODE FOUND ONLINE BELOW ) 

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

3. GET CODE TO DOWNLOAD TEMPLATE AS PDF AFTER MERGING 
