# Camunda Java 7.21

## Requirements
- Java Runtime Environment 1.8+
- Camunda Platform
- Camunda Modeler

## BPM Notation
- Start Event : BPMN elements that initiate the execution of a process instance
- None/End Event : BPMN elements that represent the termination or completion points of a business process.

### Start Event
- None : Process can be started manually, typically by a user or an external system
- Message : Process automatically started by receiving a specific message.
- Timer : Process automatically started at a specified time or after a defined duration
- Signal : Process automatically started by receiving a specific signal
- Conditional : Process instance starts when the specific condition evaluates to be true

### None/End Event
- None : Normal termination point of the process
- Message : send a specific message when the process reaches its completion.
- Signal : send a specific signal when the process reaches its completion
- Terminate : forcefully terminate the process instance when it reaches this point
- Error : represents the termination of a process due to an error or exceptions

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

### Add Start Event
- Click on start event
- Context menu will open
- Select the event shape
- Set the start event properties

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

## Configure the Service Task
- Open the properties panel
- Click on the activity
- Click `Implementation`
- Change the `Type` to `External`
- Add the `Topic`

### Configure Properties
- Open the properties panel
- Click `General`
- Add the `Name`
- Add the `ID`
- Mark the process to be `Executable`

### Hello World
- Create an event
- Select General
- Script Format : Groovy
- Script Type : Inline Script
- Script : `println "Hello World"`
