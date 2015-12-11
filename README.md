Conference Central for the Udacity Project 4

## Products
- [App Engine][1]

https://full-stack-conference.appspot.com/#/
## Language
- [Python][2]

## APIs
- [Google Cloud Endpoints][3]

## Setup Instructions
1. Update the value of `application` in `app.yaml` to the app ID you
   have registered in the App Engine admin console and would like to use to host
   your instance of this sample.
2. Update the values at the top of `settings.py` to
   reflect the respective client IDs you have registered in the
   [Developer Console][4].
3. Update the value of CLIENT_ID in `static/js/app.js` to the Web client ID
4. (Optional) Mark the configuration files as unchanged as follows:
   `$ git update-index --assume-unchanged app.yaml settings.py static/js/app.js`
5. Need to change the Client-ID for Google Sign Up API. 
Line 89 in app.js

1. Run the app with the devserver using `dev_appserver.py DIR`, and ensure it's running by visiting your local server's address (by default [localhost:8080][5].)
1. (Optional) Generate your client library(ies) with [the endpoints tool][6].
1. Deploy your application.



# Conference Organization App API Project

### About

This project is a cloud-based API server to support a web-based and native Android application for conference organization.  The API supports the following functionality:

- User authentication (via Google accounts)
- User profiles
- Conference information
- Session information

The API is hosted on Google App Engine as application ID [conference-app-fullstack](https://conference-app-fullstack.appspot.com/#/), and can be accessed via the [API explorer](https://apis-explorer.appspot.com/apis-explorer/?base=https://conference-app-fullstack.appspot.com/_ah/api#p/).


### Useful resources
- [Udacity Git Hub](https://github.com/udacity/fullstack-nanodegree-conference/blob/master/models.py)
- [Google App Engine Python Docs](https://cloud.google.com/appengine/docs/python/)
- [Programming Google App Engine (Book)](http://www.amazon.com/Programming-Google-App-Engine-Sanderson/dp/144939826X)
- [Data Modeling for Google App Engine Using Python and ndb (Screencast)](https://www.youtube.com/watch?v=xZsxWn58pS0)
- [App Engine Modeling: Parent-Child Models (GitHub)](https://github.com/GoogleCloudPlatform/appengine-modeling-ndb/blob/master/parent_child_models.py)


### Design and Improvement Tasks

#### #1 Add Sessions to a Conference

Conference.py contains corresponding endpoints and methods.
I added the following endpoint methods in conferencepy

- `createSession`:    given a conference, creates a session.
- `getConferenceSessions`:   given a conference, returns all sessions.
- `getConferenceSessionsByType`:   given a conference and session type, returns all applicable sessions.
- `getSessionsBySpeaker`: given a speaker, returns all sessions across all conferences.

[1]: https://developers.google.com/appengine
[2]: http://python.org
[3]: https://developers.google.com/appengine/docs/python/endpoints/
[4]: https://console.developers.google.com/
[5]: https://localhost:8080/
[6]: https://developers.google.com/appengine/docs/python/endpoints/endpoints_tool
