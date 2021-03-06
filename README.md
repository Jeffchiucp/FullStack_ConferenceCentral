Conference Central 

## Products
- [Google App Engine][1]

https://conference-app-fullstack.appspot.com/#
## Language
- [Python]
- [JavaScript]
- [HTML]
- [CSS]

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
- [Google App Engine Python Docs](https://cloud.google.com/appengine/docs/python/)
- [Programming Google App Engine (Book)](http://www.amazon.com/Programming-Google-App-Engine-Sanderson/dp/144939826X)
- [Data Modeling for Google App Engine Using Python and ndb (Screencast)](https://www.youtube.com/watch?v=xZsxWn58pS0)
- [App Engine Modeling: Parent-Child Models (GitHub)](https://github.com/GoogleCloudPlatform/appengine-modeling-ndb/blob/master/parent_child_models.py)

Task 1: Add Sessions to a Conference

Overview

Sessions can have speakers, start time, duration, type of session (workshop, lecture etc…), location. You will need to define the Session class and the SessionForm class, as well as appropriate Endpoints.
You are free to choose how you want to define speakers, eg just as a string or as a full fledged entity.
Define Session class and SessionForm

In the SessionForm pass in:
Session name
highlights
speaker
duration
typeOfSession
date
start time (in 24 hour notation so it can be ordered).
Ideally, create the session as a child of the conference.
Define the following Endpoints methods

getConferenceSessions(websafeConferenceKey) -- Given a conference, return all sessions
getConferenceSessionsByType(websafeConferenceKey, typeOfSession) Given a conference, return all sessions of a specified type (eg lecture, keynote, workshop)
getSessionsBySpeaker(speaker) -- Given a speaker, return all sessions given by this particular speaker, across all conferences
createSession(SessionForm, websafeConferenceKey) -- open only to the organizer of the conference
Explain your design choices

Explain in a couple of paragraphs your design choices for session and speaker implementation
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


