# Accessible Video Editor
## Jump to
* [Project Info](#project-info "Goto project-info")
* [R1 Contributions](#r1-contributions "Goto r1-contributions")
* [Installation Info](#installation-info "Goto installation-info")
* [UI Documentation](#ui-documentation "Goto ui-documentation")

## Project Info
This project is ongoing from previous quarters. As a result our github classroom space is not the repository where our work is done, but rather where we have uploaded snapshots for each assignment requirement. If you would like to navigate to the main repository [click here](https://github.com/wwu-webtech/ave "goto github.com/wwu-webtech/ave").
### Course and Team
#### Course
CSCI 497T with Professor Elglaly

#### Team Members Spring 2024
- Thai Nguyen
- Alex Kefer
- Charles Mikkelborg

#### Previous Team Members
- Robin Balatbat
- Ian Cullum
- Sam Dobesh
- Nick Harang
- Kale Kurtzhall

## Features
### New Additions
#### Styling
One of the largest feature changes for this project was to polish the look and feel of the app by incorporating Ashlar components and theme into the application so that it is in line with the look and feel of a Western webpage. This redesign is one of our primary requirements in order to bring it to a deployable state. The Ashlar components also feature a pre-header section that handles theme and font setting preferences that make the original app's accessibility section redundant and so they have been removed. Keyboard shortcuts are now always on by default in lieu of their section's removal.
#### Navigation
Navigation has been redesigned so it is consistant accross all pages and all pages share the same theme, Western's website theme, as to comply with WCAG 2.1 criterion 3.2.3 and guidline 3.2 in general. The timeline and mark info display has also been adjusted to allow for tabbing between the different items instead of all items being treated as a single element. This adds additional accessibility support for those navigating by keyboard.
#### Alerts
The Alerts window originally appeared above and to the right of a shortcuts menu which has since been removed and displayed the most recent alert to the client. This area was positioned at the top of the screen above the player. It now appears to the right of the select file or player window depending on their journey through the app. It also now features the entire history of alerts via a tabled entry and grows until it is equal in height to the player where it will then turn into a scrollable section. Each entry now includes the time, in the format of hours, minutes, and seconds, at which the alert was first displayed so that the client now has a history of their alerts and actions to reference back on. It also now has the added benefit of being downloadable through the download History Button.
### Previous Work
#### Upload Video
When selecting the "Choose File" button a open file dialog is brought up where the client can search and select a valid MP4 file (only MP4s are valid at this time). Once a file is selected the page will reflect the selction by displaying the file name above the "Choose File" button. At this point the file may be uploaded into the web app by selecting the "Upload \<filename\>" button.
#### Movie Player
Upon successful upload of the file the movie player and editor are loaded for the client to begin their work. The player has the video file name printed above the player for clarity and is followed by by the player window where the client may play and seek through the video and to the right of the player window is the alerts window that displays instructions and client actions along with the timestamp of when they were first displayed. Below the player window is the player time information, which is read as "current time time / total video time" where the time is displayed in the format minutes, seconds, and milliseconds. Beside that are the time positions of Mark 1 and Mark 2 within the video. The player buttons include "Play" (or "Pause"), "-10s", "-1s", "+1s", and "+10s". These buttons allow for easy navigation of the video by providing large a play/pause button as well as seek tools to move forward or back in 1 and 10 second increments.
#### Editor Tools
The editing tools consists of six buttons. "Add Mark 1" and "Add Mark 2" are for selecting portions of the video that the client would like to take action on. The selected portion of the video is the portion that lies between Mark 1 and Mark 2. Once a portion of the are has been selected by marking its boundaries, the client may select "Play Selection" to only play the selected portion, "Trim To Selection" to remove out everything but the selected portion, and "Delete Selection" to remove out only the selected portion. After all editing is complete the client may choose ""Download \<filename\>" to retrieve a copy of their edited video.

## R1 Contributions
- Thai Nguyen
    - Styling
        - Incorporated Ashlar components and theme into the application to make it look and feel more like a Western page.
        - The Ashlar pre-header now handles the theme change and font change.
    - Timeline
        - Adjusted timeline to be more spaced out and distinct from the progress bar.
        - Added accessible labels to the current time, marker 1, and marker 2 text and made them tabbable.
    - Navigation
        - Reformatted the navigation to be consistent across all pages to comply with WCAG 2.1 criterion 3.2.3
- Alex Kefer
- Charles Mikkelborg
    - Alerts
        - Added Timestamps to alert messages that display HH:MM:SS that an alert was posted.
        - A bulleted history of alerts displays instead of only a single alert message at a time. This list grows as more messages are added.
        - The session's alert history may now also be downloaded using the download history button, which downloads a text file with each message on it's own line.
    - Introduction
        - An introduction has now been added that provides helpful instructions to navigate and use the app.
    - Put together UI documentation

## Installation Info
### Dependencies
Requires Python 3 and Flask.

Install flask and Flask-Reuploaded with pip (or conda) in a virtual environment.
Note that for Conda, you will have to install pip to the Conda environment, and then call pip from the environments bin folder. The path to the folder `anaconda` may be different on your system, but it installs to your home directory by default.

#### Linux

##### Pip
```
python3 -m venv env
source env/bin/activate
pip install flask Flask-Reuploaded moviepy
```

##### Conda
```
conda create --name env
conda activate env
conda install pip
~/anaconda/envs/env/bin/pip install flask Flask-Reuploaded moviepy
```

#### Windows PowerShell
```
py -3 -m venv venv
venv\Scripts\activate
pip install flask Flask-Reuploaded moviepy
```

### Quick Start
The following scripts will run AVE locally on your computer in debug mode.

#### Bash Script
```
./run
```

#### CMD Script
```
./run.cmd
```

#### PowerShell Script
```
./run.ps1
```

### Live Test
This runs the app on port 8080 for external access. Intended for testing with remote participants

#### Bash Script
```
./run_live
```

#### CMD Script
```
./run_live.cmd
```

#### PowerShell Script
```
./run_live.ps1
```

### Clean
This script exists to clear out the upload folder.
```
./clean
```

#### Manually
Run each code line from the script associated with your terminal.
If your terminal scripting language is not supported you can do the following.
Create two environment variables, `FLASK_ENV` and `FLASK_APP`.
Set `FLASK_ENV` to `development` and `FLASK_APP` to `main`. 
Then start the website locally with `flask run`.

## UI Documentation

### Landing
ID: ave_landing
![alt text](static/images/aveLanding.jpg)

### About
ID: ave_about
![alt text](static/images/aveAbout.jpeg)

### Upload
ID: ave_upload<br />
The system feature that this screenshot represents is the Upload Video feature. 
The input field has a form label associated with it complying with WCAG success criteria 2.4.6. The upload button is initially disabled and will remain so if there is no file inputted. After a file is inputted, the upload button will be able to be interacted with and when clicked will trigger the upload process. The button complies with WCAG success criteria 2.5.3 and conform for the color contrast ratio of 4.5 to 1.
![alt text](static/images/aveUpload.jpeg)

### Editor
ID: ave_editor<br />
The system feature that this screenshot represents is the Editor Tools, Alerts, and Movie Player feature. 
We designed the editor to be keyboard accessible which means the entire interface can be navigated and interacted with using only the keyboard.
The interface is also screen reader accessible which makes it usable for people who are blind or visual impaired. The UI uses simple and clear language that is easy to understand.
It also uses a high contrast color scheme and easy of read fonts that can be customized to fit the user's needs. The alerts box to the right of the screen keeps track of user and system actions and has a time attached to each action to provide an accurate timeline of user activity. This log can be downloaded as well. 
Within the editor tools, the user has access to 5 rows of controls and information. The first being an input field that dictates the current position of the video. The input field has aria labels attached to it make it accessible to screen readers complying with WCAG success criteria 3.3.2. The second row has tabbable information such as the current of the input field in comparison to the full length of the video, marker 1's position, and marker 2's position. Row 3 has the aria label of 'Play Head' as it is contains the controls for the video player. From left of right, the buttons are Play, rewind 10 seconds, rewind 1 second, forward 1 second, and forward 10 second. All these controls comply with WCAG success criteria 2.5.3. The fourth row contains buttons that facilitate editing the video. There are 5 buttons in this row with 3 being initially disabled to prevent errors. The first two buttons allow the user to place markers 1 and 2 which are times in the video that the users wants to edit. Above marker 1 and 2 being placed, the remaining 3 buttons will then be usable. The 'Play Selection' button will play the video from marker 1 to marker 2, the 'Trim to Selection' button will remove any parts of the video not with the times of marker 1 and 2. The last button 'Delete Selection' will remove any parts of the video within the times of marker 1 and 2. The last row only has one button that will download the editted video to the user's downloads folder. Like in row 3, all the buttons in row 4 and 5 comply with WCAG success criteria 2.5.3 and each row has aria labels associated it them. The alerts contains a table that contained the time an action occurred and the action itself.
![alt text](static/images/AveEditor.jpeg)
