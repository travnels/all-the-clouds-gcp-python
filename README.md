# all-the-clouds-gcp-python

## Auto Deployment from Github commit:
- Had to setup GitHub Build Trigger (Container Registry > Build Triggers > Add Trigger)
- Got this error: 
```ERROR: (gcloud.app.deploy) User [388528582146@cloudbuild.gserviceaccount.com] does not have permission to access app [all-the-clouds-gcp-python] (or it may not exist): App Engine Admin API has not been used in project all-the-clouds-gcp-python before or it is disabled. Enable it by visiting https://console.developers.google.com/apis/api/appengine.googleapis.com/overview?project=all-the-clouds-gcp-python then retry. If you enabled this API recently, wait a few minutes for the action to propagate to our systems and retry.```
Followed the link to enable it. This took a few minutes to propagate in the system.
- Added Role, `App Engine > App Engine Admin` to `388528582146@cloudbuild.gserviceaccount.com`(`Google APIs service account`) on the IAM screen
