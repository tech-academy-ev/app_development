# Curriculum
The app track includes six dates in which participants are introduced to app development with Flutter and have the chance to support each other in app development. The following bullet points are intended to give an overview of the course and provide more information about the app development track.

#### 4.1 Kick-Off Workshop (27.04.2022)
- Introduction of Udemy course (see below)
- Get to know other participants

!!! todo "Sprint 0"
    
    - Work on Udemy Course (Section 1-3)


#### 4.2 Flutter Coding Introduction (xx.xx.2022)
- Participants are expected to have completed Udemy Course Section 1-3 until today
- Explanation of Flutter & Dart basics.
- Difference Stateless and Stateful Widget
- initState and setState method
- Introduction to most important widgets

!!! todo "Sprint 1"
    
    - Work on Udemy Course (Section 4)


#### 4.3 Coding MeetUp 1 (18.05.2022)
Participants are expected to have completed Udemy Course Section 4 until today
Brief Introduction to git
Introduction to “SharedPreferences” (Local Storage)
Presentation of the project (see below)

!!! todo "Sprint 2"
    
    - Setting up the project
    - Work on the bottom bar. Make sure you can navigate to each page.
    [https://api.flutter.dev/flutter/material/BottomNavigationBar-class.html](https://api.flutter.dev/flutter/material/BottomNavigationBar-class.html)
    - Add two text fields and a “save” button on the “add-notes” page. 
    Make sure you had created a Form() and added a FormKey [https://docs.flutter.dev/cookbook/forms/validation](https://docs.flutter.dev/cookbook/forms/validation) 


#### 4.4 Coding MeetUp 2 (01.06.2022)
Flutter Tips by Steffen
Discussion about the project and you can ask for help
If you have not completed the recommended tasks, do not hesitate to reach out for help.

!!! todo "Sprint 3"
    
    - Add a validator function to each text field [https://docs.flutter.dev/cookbook/forms/validation](https://docs.flutter.dev/cookbook/forms/validation)
    - Use [https://pub.dev/packages/shared_preferences](https://pub.dev/packages/shared_preferences) to save the data locally.
    - Work on the “view-notes”-page (page1): make sure you create a Stateful widget and check whether you have saved data every time you open the page. Make the check in the initState() method. If data is available, use the setState() function to update your String variables. The following guideline may help: [https://docs.flutter.dev/cookbook/persistence/key-value](https://docs.flutter.dev/cookbook/persistence/key-value) 
    - If the Strings are not null, display a note-widget with the retrieved data.


    Attention: It is fine if the user can only save one note. As soon as a new note is entered the previous note can be overwritten. You do not have to implement the logic of adding an unlimited number of notes.

#### 4.5 Coding MeetUp 3 (15.06.2022)
Discussion about the project and the participants will have the chance to ask for help
If you have not completed the recommended tasks, do not hesitate to reach out for help.

!!! todo "Sprint 4"
    
    - Add both web-views (see [https://codelabs.developers.google.com/codelabs/flutter-webview#3](https://codelabs.developers.google.com/codelabs/flutter-webview#3))
    - Add the “edit-profile” feature and make sure you use Forms() and a StatefulWidget again.


#### 4.6 Coding MeetUp 4 (29.06.2022)
Discussion about the project and the participants will have the chance to ask for help
If you have not completed the recommended tasks, do not hesitate to reach out for help.


!!! todo "Sprint 5"
    
    - Working on last details and making sure all requirements are met


## Deadline: Hand-In on 03.07.2022