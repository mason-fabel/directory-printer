directory-printer
=================

Web app to generate a church directory pdf using the planning center apis.

FAQs
----

1. How do I clear the cache?
    - Make sure you are logged into correct google account
    - Go to [Google Cloud Services](https://console.cloud.google.com)
    - Select project "directory-export-pdf"
    - Open "Hamburger" menu top left
    - Select Storage >> Browser
    - Open "directory-export-pdf.appspot.com"
    - Delete all contents. There should be a directory with a number (e.g. "217317")
2. How do I deploy the app?
    - Navigate to code directory in terminal
    - Run `gcloud app deploy app.yaml`
    - Run `gcloud app deploy app_directory.yaml`
4. How do I take down the app?
    - Navigate to google cloud console in browser, find the app versions and delete
    - Alternatively, run the following commands
        - Run `gcloud app services delete default`
        - Run `gcloud app services delete hinson"`

Helpful Links
-------------
- [Planning Center lists](https://people.planningcenteronline.com/lists)
- [Google cloud console](https://console.cloud.google.com)
- [Hinson app url](https://directory-export-pdf.appspot.com)
- [Hinson service url (_don't navigate here_)](https://hinson-dot-directory-export-pdf.appspot.com)

Other references
----------------
- [Info regarding google cloud storage signed URLs](https://cloud.google.com/storage/docs/access-control/signed-urls)
- Planning center callback url looks something like this: `https://hinson-dot-directory-export-pdf.appspot.com/api/v1/authorize`
