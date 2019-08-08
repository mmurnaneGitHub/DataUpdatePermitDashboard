# DataUpdatePermitDashboard
Files for updating data used by the application Tacoma Permit Dashboard: https://wspdsmap.cityoftacoma.org/website/PDS/PermitDashboard/

Updates json, csv, and AGOL web map for application.

Needs a 'log' subfolder in the same directory as these files.

1. UpdateIssued.py downloads last 30 days of issued permits from CivicData as json, converts to csv, and updates AGOL csv which in turn updates web map.
2. UpdateNewApplications.py downloads last 30 days of new permit applications from CivicData as json, converts to csv, and updates AGOL csv which in turn updates web map.
3. Send_Email.vbs send email with results of running UpdateIssued.py and UpdateNewApplications.py.
4. UpdateData.bat makes a backup copy of yesterday's files into 'log' subfolder and then runs UpdateIssued.py, UpdateNewApplications.py, and Send_Email.vbs.
