Please make sure you have a tool for previewing markdown files properly. Here's the link to the VSCode extensio: https://code.visualstudio.com/docs/languages/markdown#_markdown-preview

# Setup

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

Your task is to build a student timeline component as shown in the below image. The timeline displays all the student activities.
You can find the full spec, screenshots and APIs below.

# Requirements:

- The main feed is API #V1
- The timeline is grouped and ordered by months
- Each activity has it's own set of settings. Available activities and their settings are listed below
- It should support the following routes:
  - The main student timeline as shown in [Image 1](Timeline)
  - Zoom activity. [Image 2](Zoom)
- It should support two types of filters:
  - Free text filter
  - Activity type filter
- It should support pagination for loading more activities in the form of a 'load more' button

# Bonus

- The app needs to work with another feed, API #V2, that has a different structure. Make sure your code support that

# APIs

- V1: http://localhost:3000/student/:student_id:/activities/v1
- V2: http://localhost:3000/student/:student_id:/activities/v2

# Images

1. Activities view
   ![Timeline](assets/timeline.jpg)
2. Zoom view
   ![Zoom](assets/zoom.jpg)

# Activity Types and Settings

##### Every activity has two settings. It can be scorable and it can be viewed in zoom mode (View work button).

- Movie
  - Score = false
  - Zoom = false
- Quiz
  - Score = true
  - Zoom = true
- Easy Quiz
  - Score = true
  - Zoom = true
- Challenge
  - Score = true
  - Zoom = true
- Make a Map
  - Score = false
  - Zoom = true
- Make a Movie
  - Score = false
  - Zoom = true
- Wordplay
  - Score = false
  - Zoom = true
- Related reading
  - Score = false
  - Zoom = false
- Draw about it
  - Score = false
  - Zoom = true
