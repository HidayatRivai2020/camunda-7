# Camunda Java 7.13
- Requirement
  - Camunda Modeler
  - Camunda BPM run
  - Apache Tomcat + WildFly / Spring Boot

## Taskbar

### Run Camunda modeler
- Open camunda modeler
- select camunda version 7
- select BPMN Diagram

### Create a new BPMN Diagram
- Click `File`
- Click `New File`
- Click `BPMN Diagram (Camunda 7).`

### Save the BPMN Diagram
- Click `File`
- Click `Save` to save the file
- Click `Save As` to save the file in new location
- Click `Save All` to save All files

### Deploy the BPMN Diagram
- Click `Deploy Current Diagram`
- Set `Deployment Name`
- Set `Tenant ID`
- Set `REST Endpoint`
- Click `Deploy` to deploy current diagram
- Click `Cancel` to cancel deploy
- `Deployment succeeded` notification if deployment success

## Event & Activity

### Change Event Name
- Double click on event
- A text box will open
- Update the name in the text-box
- `shift + Enter` to add line breaks

### Add Activity
- Click on object
- Context menu will open
- Select the activity shape
- Update the name

### Change Object Type
- Click on object
- Click the `Change Type` button (Wrench Icon Button)
- Select the object type

### Remove Object
- Click on object
- Click the `Remove Object` button (Trash Can Icon Button)
- Select the object type

### Configure Properties
- Open the properties panel
- Click `General`
- Add the `Name`
- Add the `ID`
- Mark the process to be `Executable`
