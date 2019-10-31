<p style="font-weight:600; font-size:36px">TABLE OF CONTENT</P>

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Environment Setup](#environment-setup) - [Client](#client) - [Server](#server)
- [Assignment](#assignment)
- [Requirements & Guides:](#requirements-guides)
- [Bonus](#bonus)
- [APIs](#apis)
- [Screenshots](#screenshots)
  - [Activities view](#activities-view)
  - [Zoom view](#zoom-view)
- [Activity Types and Settings](#activity-types-and-settings)

<!-- /code_chunk_output -->

# Environment Setup

##### Client

1. Navigate to your client folder: `cd {project folder}/client`
2. Install project dependencies: `npm install`
3. Run your dev server. `npm run serve`. Your dev server is ready at http://localhost:8080
   (The dev server defaults to port 8080. If it's taken and it uses a different one you'll need to update your cors settings in the server app.js)

##### Server

1. Navigate to your server folder: `cd {project folder}/server`
2. Install project dependencies: `npm install`
3. Run your server. `DEBUG=server:\* npm start`. Your server is ready at http://localhost:3000

---

# Assignment

Your task is to build a student timeline component as shown in image #1. The timeline displays all the student activities.
You can find the full spec, screenshots and APIs below.

# Requirements & Guides:

- There are two main views in this app. [Activities view](#activities-view) and [Zoom view](#zoom-view).
- The main activities feed you should be using is the V1 [APIs](#apis)
- The activities timeline should be grouped and ordered by months
- Each activity has it's own set of settings. Available activities and their settings are listed in the [Activity Types and Settings](#activity-types-and-settings) below
- The app should support direct access to the zoom view via your router
- The app should support two types of filters:
  - Free text filter
  - Activity type filter
- The app should support pagination for loading more activities in the form of a 'Load more' button
- When the user clicks on the 'View work' link it should open the zoom view

# Bonus

1. The app needs to work with another feed, [APIs](#apis) #V2, that has a different structure. Make sure your code supports both structures.
2. Add support for hiding activities. This should be persistent.
3. Add autocomplete support to the text filter input. You can use you main API feed for that.

# APIs

- V1: http://localhost:3000/student/:student_id:/activities/v1
- V2: http://localhost:3000/student/:student_id:/activities/v2

# Screenshots

###Activities view
![Timeline](assets/timeline.jpg)
###Zoom view
![Zoom](assets/zoom.jpg)

# Activity Types and Settings

Every activity has two settings. They can be scored and they can be viewed in zoom mode (View work button). Those settings are not a part of the API response but resides on the client app.

- **Movie**
  - Score = false
  - Zoom = false
- **Quiz**
  - Score = true
  - Zoom = true
- **Easy Quiz**
  - Score = true
  - Zoom = true
- **Challenge**
  - Score = true
  - Zoom = true
- **Make a Map**
  - Score = false
  - Zoom = true
- **Make a Movie**
  - Score = false
  - Zoom = true
- **Wordplay**
  - Score = false
  - Zoom = true
- **Related reading**
  - Score = false
  - Zoom = false
- **Draw about it**
  - Score = false
  - Zoom = true
