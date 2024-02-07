# Camunda BPMN Run

## Structure Files
- camunda-h2-default : folder created after starting camunda
    - proccess-engine.mv.db : database file
- configuration : Configuration folder
    - keystore
    - resource : user resource for process model
    - sql : SQL Folder
        - create : folder with sql files to create the tables in database
        - drop : folder with sql files to delete the tables in database
        - upgrade : folder with sql files to upgrade the tables in databse
    - userlib : user library folder
    - default.yml : default configuration file
    - production.yml : produciton configuration file
- internal : internal folder
    - rest : camunda REST libraries folder
    - webapps : camunda webapps libraries folder
    - camunda-bpm-run-core.jar : camunda bpm library
- LICENSE : License file
- LICENSE-BOOK-7.13.0.txt : License Book file
- NOTICE : important information file
- README.md : documentation file
- start.bat : file to start camunda for windows
- start.sh : file to start camunda for linux or mac

## Run Camunda
- Open camunda bpmn run
- Execute start.sh
- access url : localhost:8080/
- access default index : http://localhost:8080/camunda-welcome/index.html

### Default Index
- Login Page:
  - default user : Demo
  - default pass : Demo
- Webapps
  - Task-list : Complete Task List
  - Cockpit : On-Going Task in Engine
  - Admin : Manage user and permissions
  - Welcome : Welcome page after login
- Invoice Example : Example of Camunda BPM features guided by a simple invoice processs
- Modeler : BPMN Modeler page
- Documentation : URL for offical documentation
- Forum : Camunda Forum

### Camunda Welcome
- Application : Main Application
  - Cockpit : On-Going Task in Engine
  - Task-list : Complete Task List
  - Admin : Manage user and permissions
- Profile : User Profile
  - Edit Profile : Edit the data of user
  - Change Password : update into new password
- Links : Documentation Link

### Deploy BPMN every run
- Create a BPMN File
- Save the file in `resource` folder
- Run Camunda

## Cockpit

### Check deployed process
- Click **number** on Deployed or Click `Processes`
- Click process **name** link to start

## Task-list
- Keyboard Shortcut : Shortcut using keyboard button
- Create Task : Create Task and assign to any individual
- Start Process : Start an existing process
- User : User with name
  - My Profile : Open Welcome Page
  - Sign Out : Sign Out from current session
- Other Page : Link to go to another page
  - Admin : Open admin page
  - Cockpit : Open cockpit page

### Check process
- Click `Add a simple filter`
- Select a process

### Create Task
- Click `Start process`
- Set Variable (Optional)
- Click `Start` to start the process
- Click `close` to cancel process

### Start process
- Click `Start process`
- Click process definition deployed **name** link
- Set Variable (Optional)
- Click `Start` to start the process
- Click `back` to go back
- Click `close` to cancel process

