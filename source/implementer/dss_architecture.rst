Architecture of decision support system
========================================

We are designing decision support application to be provide almost all functionality directly from the android app without depending much
 on the server too much. We feel this is required to provide best user experience to the end users - who may not have Internet access for
 days.

There are two runtime components required for decision support feature - apache web server (or like) and android app. We have not
introduced OpenMRS into the mix yet but we are following its REST contract for concept load. Web server hosts static files for concepts,
questionnaire json and decision support JS files. Android app fetches these files from the server on startup and on regular sync. Android
 app also allows the user to upload the saved questionnaires (with answers) to the web server.

Android app comes with offline database on the device. All the user's work is saved in this database. When the user chooses to upload the
 data to the server, the app reads the data from local db, converts it into a csv format and uploads.