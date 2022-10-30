# Curriculum
The app track includes six dates in which participants are introduced to app development with Flutter and have the chance to support each other in app development. The following bullet points are intended to give an overview of the course and provide more information about the app development track.

#### 4.1 Kick-Off Workshop (23.11.2022)
- Introduction of Udemy course (see below)
- Get to know other participants

!!! todo "Sprint 0"
    
    - Work on Udemy Course (Section 1-3)
    - As explained in secion 1 of the udemy course, install and setup flutter:
    1. Install Flutter and its dependencies [https://docs.flutter.dev/get-started/install/windows](https://docs.flutter.dev/get-started/install/windows) / [https://docs.flutter.dev/get-started/install/macos](https://docs.flutter.dev/get-started/install/macos)
    2. Open your terminal -> enter `flutter doctor` and verify no issues need to be resolved
    3. Install VS Code and the extensions "flutter" and "dart"


#### 4.2 Flutter Coding Introduction (09.11.2022)
- Participants are expected to have completed Udemy Course Section 1-3 until today
- Explanation of Flutter & Dart basics.
- Difference Stateless and Stateful Widget
- initState and setState method
- Introduction to most important widgets

!!! todo "Sprint 1"
    
    - Work on Udemy Course (Section 4)


#### 4.3 Coding MeetUp 1 (23.11.2022)
- Participants are expected to have completed Udemy Course Section 4 until today

- Brief Introduction to git
- Introduction to “SharedPreferences” (Local Storage)
- Presentation of the project (see below)

!!! todo "Sprint 2"
    
    1. Setting up the project: Use `flutter create <your_project_name>
    2. open lib/main.dart
    3. Delete the entire Stateful "MyHomePage" Widget
    4. Create a new file: "home_page.dart"
    5. Open "home_page.dart" and type "st" --> autocomplete-window will pop-up: choose: stateful widget and enter HomePage
    6. Let the HomePage Widget return a Scaffold widget instead of a container
    7. Add "AppBar()" within `appBar:` and choose a title
    8. Create 4 new files, each with an own stateless widget and individual name. (view note, add note, web view 1, web view 2)
    9. Add a bottom bar. Here you can find an example:
    [https://api.flutter.dev/flutter/material/BottomNavigationBar-class.html](https://api.flutter.dev/flutter/material/BottomNavigationBar-class.html)
    Make sure that the click on each button within the bottomBar will display the widget from the 4 recently created files.
    10. In the widget of the the add-note page, add a Form() widget. Wihtin the Form widget add a Column with two text fields and a “save” TextButton.  You can find an example here:
    11. Make sure you had created a Form() and added a FormKey [https://docs.flutter.dev/cookbook/forms/validation](https://docs.flutter.dev/cookbook/forms/validation) 


#### 4.4 Coding MeetUp 2 (14.12.2022)
- Flutter Tips by Steffen
- Discussion about the project and you can ask for help
- If you have not completed the recommended tasks, do not hesitate to reach out for help.

!!! todo "Sprint 3"
    
    1. Add a validator function to each text field. See [https://docs.flutter.dev/cookbook/forms/validation](https://docs.flutter.dev/cookbook/forms/validation). Make sure that the user can only save, when the text fields are not empty
    2. Use [https://pub.dev/packages/shared_preferences](https://pub.dev/packages/shared_preferences) to save the data locally.
    3. Work on the “view-notes”-page: make sure you create a Stateful widget and check whether you have saved data every time you open the page. To do that, make the check in the initState() method. create a nullable String variable `String? savedNoteTitle;` and `String? savedNoteContent;` If data is available, use the setState() function to update both variables. The following guideline may help: [https://docs.flutter.dev/cookbook/persistence/key-value](https://docs.flutter.dev/cookbook/persistence/key-value) 
    4. If the Strings are not null, display a note-widget with the retrieved data. You can do that by using a condition: `savedNoteTitle != null ? Text(savedNoteTitle) : const SizedBox()`. This means that you want to show a text widget if the variable is not null and an empty constant sizedbox if the variable is null. Do the same for the savedNoteContent variable. Make sure you have added both within the same column widget.

    Attention: It is fine if the user can only save one note. As soon as a new note is entered the previous note can be overwritten. You do not have to implement the logic of adding an unlimited number of notes.
    

#### 4.5 Coding MeetUp 3 (11.01.2023)
- Discussion about the project and the participants will have the chance to ask for help
- If you have not completed the recommended tasks, do not hesitate to reach out for help.

!!! todo "Sprint 4"
    
    - Add both web-views (see [https://codelabs.developers.google.com/codelabs/flutter-webview#3](https://codelabs.developers.google.com/codelabs/flutter-webview#3)).
    - Add the “edit-profile” feature and make sure you use Forms() and a StatefulWidget again. The concept is the same.


#### 4.6 Coding MeetUp 4 (01.02.2023)
- Discussion about the project and the participants will have the chance to ask for help
- If you have not completed the recommended tasks, do not hesitate to reach out for help.


!!! todo "Sprint 5"
    
    - Working on last details and making sure all requirements are met. 


## Deadline: Hand-In on 04.02.2023 (11.59PM)
