# Camunda Java 7.20

## Requirement
- Camunda Modeler
- Camunda BPM run
- Apache Tomcat + WildFly / Spring Boot

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

## Camunda BPMN Run

### Run Camunda
- Open camunda bpm run
- Execute start.sh
- access url : localhost:8080/
- login using data in default.yml
  - user : demo
  - password : demo

### Camunda Welcome
- Application : Main Application
  - Cockpit : On-Going Task in Engine
  - Task-list : Complete Task List
  - Admin
- Profile : User Profile
- Links : Documentation Link

### Deploy BPMN every run
- Create a BPMN File
- Save the file in `resource` folder
- Run Camunda

### Cockpit

#### Check deployed process
- Click **number** on Deployed or Click `Processes`
- Click process **name** link to start

### Task-list

#### Check process
- Click `Add a simple filter`
- Select a process

#### Start process
- Click `Start process`
- Click process definition deployed **name** link
- Set Variable (Optional)
- Click `Start` to start the process
- Click `back` to go back
- Click `close` to cancel process


## Camunda Modeler

### Taskbar

#### Run Camunda modeler
- Open camunda modeler
- select camunda version 7
- select BPMN Diagram

#### Create a new BPMN Diagram
- Click `File`
- Click `New File`
- Click `BPMN Diagram (Camunda 7).`

#### Save the BPMN Diagram
- Click `File`
- Click `Save` to save the file
- Click `Save As` to save the file in new location
- Click `Save All` to save All files

#### Deploy the BPMN Diagram
- Click `Deploy Current Diagram`
- Set `Deployment Name`
- Set `Tenant ID`
- Set `REST Endpoint`
- Click `Deploy` to deploy current diagram
- Click `Cancel` to cancel deploy
- `Deployment succeeded` notification if deployment success

### Event & Activity

#### Change Event Name
- Double click on event
- A text box will open
- Update the name in the text-box
- `shift + Enter` to add line breaks

#### Add Activity
- Click on object
- Context menu will open
- Select the activity shape
- Update the name

#### Change Object Type
- Click on object
- Click the `Change Type` button (Wrench Icon Button)
- Select the object type

#### Remove Object
- Click on object
- Click the `Remove Object` button (Trash Can Icon Button)
- Select the object type

#### Configure Properties for Execution
- Open the properties panel
- Click `General`
- Add the `Name`
- Add the `ID`
- Mark the process to be `Executable`

