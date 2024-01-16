# [Camunda 7](https://docs.camunda.org/manual/7.20/)
- Light-weight and open-source platform for Business Process Management
- Current Version: 7.20

# Camunda QuickStart

## Installing Camunda
- Install <b>Java Runtime Environment 1.8+</b>
- Install Camunda Platform
- Install Camunda Modeler
- Execute Camunda Modeler

## [Executable Process](https://github.com/HidayatRivai2020/camunda-7/blob/main/payment.bpmn) 

### Create a new BPMN Diagram
- Click `File`
- Click `New File` 
- Click `BPMN Diagram (Camunda Platform).`

### Start with a Simple Process
- Changing Name
    - Double click on event
    - A text box will open
    - Update the name in the text-box
    - `shift + Enter` to add line breaks
- Add Activity
    - Click on object
    - Context menu will open
    - Select the activity shape
    - Update the name
- Change Object Type
    - Click on object
    - Click the `Change Type` button (Wrench Icon Button)
    - Select the object type

### Configure the Service Task
- Using external Task Pattern
    - Open the properties panel
    - Click on the activity
    - Click `Implementation` 
    - Change the `Type` to `External`
    - Add the `Topic`

### Configure Properties for Execution
- Using external Task Pattern
    - Open the properties panel
    - Click `General` 
    - Add the `Name`
    - Add the `ID`
    - Mark the process to be `Executable`

### Save the BPMN Diagram
- Click `File`
- Click `Save` to save the file
- Click `Save As` to save the file in new location
- Click `Save All` to save All files
