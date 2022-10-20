# Project

As part of the project you will work on your own app. The idea is to build an app for Tech-Academy participants. The app provides space for tech-academy related notes and offers easy and fast access to certain pages of the Tech-Academy website. To complete this course, you are asked to meet the defined requirements. The following requirement section is divided in two parts. First, the project user-stories are presented. In software development, a user story is an informal description of features of a software product. This type of feature description is commonly used in the industry. The user stories have one or multiple acceptance criteria attached. Second, the technical requirements are listed. To complete the project and pass this track, you are asked to fulfill all acceptance criteria as well as to meet all technical requirements.

![WhatsApp Image 2022-10-20 at 11 49 00](https://user-images.githubusercontent.com/41230924/196933464-3787309d-e8f7-4c7c-8e4c-c0c8384a6330.jpeg)


## Requirements

As a TechAcademy participant, I want to manage my own TechAcademy tasks in a Flutter app. To do that, I need six features. 

#### 1. Display notes (page 1)
As a TechAcademy participant, I want to see all my previously written notes on a page. If I have saved my name on the profile page previously, I want to be welcomed by the app.


##### Acceptance Criteria:
All notes which have been added before, are visible.
If no note has been saved so far, the text "No note available" is visible.
If the user has added a name, the name is visible above the notes.



#### 2. Adding Notes (page 2)
As a TechAcademy participant, I want to have a page, on which I can submit a note title and note body text. As soon as the note is submitted, I want to see the saved note on page 1.


##### Acceptance Criteria:
A form field for the title is available
A form field for the body text is available
A save button is available
When the button is clicked, the added text will be saved locally



#### 3. Show Webview1 (page 3)
As a TechAcademy participant, I want to have a page on which the website [https://www.tech-academy.io/team/](https://www.tech-academy.io/team/) is visible. The website should load as soon as I visit the page. 


##### Acceptance Criteria:
When the page opens, the website [https://www.tech-academy.io/team/](https://www.tech-academy.io/team/) loads directly
I can navigate on the website



#### 4. Show Webview2 (page 4)
As a TechAcademy participant, I want to have a page on which the website [https://www.tech-academy.io/login/](https://www.tech-academy.io/login/) is visible. The website should load as soon as I visit the page. 


##### Acceptance Criteria:
When the page opens, the website [https://www.tech-academy.io/login/](https://www.tech-academy.io/login/) loads directly
I can navigate on the website



#### 5. Update first- and last name (page 5)
As a TechAcademy participant, I want to have a page, on which I can update my first- and last name. Both items should have an individual text field. The first and last name should only be updatable if both text fields have at least two characters entered. Only letters should be allowed to enter. As soon as the names are saved, I want to see the text “Hello”, followed by the recently saved first- and last name above my previously saved notes.


##### Acceptance Criteria:
A form field for the first name is available
A form field for the second name is available
A save button is available
When the button is clicked, the first name and last name will be saved locally
When a name is saved, the saved name is visible above my notes



#### 6. Having a Bottom-Navigation-bar
As a TechAcademy participant, I want to always have a bottom navigation bar visible. The navigation bar should have 5 buttons. Each button should take me to one of the pages.


##### Acceptance Criteria:
The Bottom navigation bar is always visible
The Bottom navigation bar has 5 buttons
When a button is pressed, the attached page is opened
