# Camunda Java 7.21
- Requirement
  - Java Runtime Environment 1.8+
  - Camunda Platform
  - Camunda Modeler
- BPM Notation
  - Events
  - Gateways
  - Tasks
  - Subprocess
  - Forms
- Extension Reference
- DMM Notation

## Events
- Start Events
  - BPMN elements that initiate the execution of a process instance
  - Starting point of a business process and define how the process will be triggered or activated
- None/End Events
  - BPMN elements that represent the termination or completion points of a business process
  - Indicate the different outcomes or states that a proces can reach at its conclusion
- Message Events
  - BPMN elements used to model the sending and receiving of messages between different parts of a business process or between the process and external systems
  - Enable communication and coordination between process activities or participants
- Timer Events
  - BPMN elements used to model time-based events within a business process
  - Enable schedule activities or actions to occur at specific points in time or after a certain duration
- Error Events
  - BPMN Elements used to handle and manage errors or exceptions that occur during the execution of a business process
  - Allow to define how errors should be caught, handled, and escalated within the process flow
- Escalation events
  - Reference a named escalation
  - Used to communicate from sub process to an upper process
  - Non critical
  - execution continues at the location of throwing
- Signal Events
  - BPMN elements used to facilitate communication and coordination between different parts of a business process or between the process and external systems
  - Allow suer to trigger actions or synchronize process flows based on the receipt of a specific signal
- Cancel and Compensation Events
  - BPMN elements used to handle the cancellation or compensation of activities within a business process
  - Provide mechanisms to undo or compensate previously executed activities when certain conditions are met
  - Can be triggered by using appropriate BPMN elements such as service task, script task or specific conditions defined in the process flow
- Conditional Events
  - BPMN elements used to model events that occur based on  the evaluation of a condition
  - Enable user to create flexible process flows where certain actions or activities are triggered or executed conditionally
- Link Events
  - Special case
  - Has no special execution semantic
  - serves as a "Go To" another point in the same process model
  - Can use two matching links as an alternative to a sequence flow as shown in the following example 
- Terminate Events
  - Ends the complete scope it raised in and all contained inner scopes
  - Useful if you have parallel token flow in a process and consume all tokens available in the same scope immediately
  - Terminate complete instance when the event on the process instance level
  - Terminate the current scope and all contained processes instance when the event on the subprocess level

### Start Events
- None Start Events
  - Process can be started manually, typically by a user or an external system
  - Does not require any specific trigger or condition to initiate the process
- Message Start Events 
  - Allow the process to be started by receiving a specific message.
  - The process instance is triggered and executed when the designated message is received
- Timer
  - Allow the process to be started at a specified time or after a defined duration
  - Allows user to schedule the process execution based on a specific time or a time interval
- Signal 
  - Allow the process to be started by receiving a specific signal
  - The process instance is triggered and executed when designated signal is received
- Conditional
  - initiates the process based on specific condition
  - the process instance starts when the specific condition evaluates to be true
  - the condition can be expressed using expressions or scripting languages supported by Camunda BPM

### None/End Events
- None End Event
  - Default end events
  - Normal termination point of the process
  - Indicating that the process has successfully completed
- Message End Events
  - Send a specific message when the process reaches its completion
  - Can be used to notify external systems or trigger subsequent processes
- Signal End Event
  - Send a specific signal when the process reaches its completion
  - Can be used to communicate with external systems or trigger subsequent processes
- Terminate End Event
  - Forcefully terminate the process instance when it reaches this point
  - Immediately ends the process execution even if there are other activities or task remaining in the process
- Error End Event
  - Represents the termination of a process due to an error or exceptions
  - Allow users to handle and report errors that occur during process of execution 

### Message Events
- Start Event
  - Initiates process instance when a specific message is received
  - Serves as the trigger for starting the process
  - The process instance started and executed when the designated message is received
- Intermediate Event
  - a point within the process where a message is expected and received
  - Can be used to trigger certain actions or to synchronize process flows based on the receipt of a specific message
- End Event
  - End a process instance when a specific message is received
  - Serves as the trigger for ending process
  - The process instance send message to receiving message event when the designed message to receiving message event

### Timer Events
- Timer Start Event
  - Initiates a process instance at a specified time or after a defined duration
  - Serves as the trigger for starting the process based on a timer
- Timer Intermediate Event
  - Represents a point within the process where a specific action or activity is triggered based on a timer.
  - Allows to delay or schedule activities within the process

### Error Events
- Error Start Event
  - Initiates a process instance when a specific error occurs
  - Serves as the trigger for starting the process based on an error
- Error Intermediate Event
  - Represents a point within the process where a specific action or activity is triggered when an error occurs.
  - Allows to catch and handle errors at specific points in the process

### Escalation Events
- Escalation Start event
  - Can only be used to trigger an event sub-process
  - cannot be used to start a process instance
- Escalation Boundary Event
  - Intermediate catching escalation event on the boundary of an activity
  - thrown within the scope of the activity on which is defined
- Escalation Intermediate Throw Event
  - Throw a named escalation when process executions arrives at this event
  - Can be caught by an escalation boundary event or an event sub-process with an escalation start event which has the same or none escalation code
- Escalation End Event
  - End the current path of execution and throw a named escalation when process executions arrives at this event
  - Same behavior with Escalation Intermediate throw event

### Signal Events
- Signal Start Event
  - Initiates a process instance when a specific signal is received
  - Serves as the trigger for starting the process based on a signal
- Signal Intermediate Event
  - Represents a point within the process where a specific action or activity is triggered upon receiving a signal
  - Allows user to synchronize or control process flows based on the occurrence of a signal
- Signal End Event
  - Ends a process instance and send a specific signal to receiving signal
  - It serves as the trigger fo ending the process based on signal

### Cancel and Compensation Events
- Cancel End Event
  - Used to cancel the executions of a subprocess or activity when it is reached
  - Terminates the associated subprocess or activity and any ongoing execution within it
  - Can be useful for cancelling or aborting parts of process when certain conditions are met
- Compensation Intermediate Event
  - Used to trigger a compensation proces or activity when it is reached
  - allows for the undoing or compensating of previously executed acitvities.
  - the process flow moves to the corresponding compensation handler when the compensation event is triggered
  - can perform the necessary actions to reverse or compensate for the completed activities

### Conditional Events
- Conditional Start Event
  - Initiates process instance when a spcific condition is met
  - Serves as the trigger for starting the process based on a condition evaluation
- Conditional Intermediate/Boundary Event
  - Represents a point within the process where a specific action or activity is triggered or executed when a condition is evaluated to true
  - Allows user to control the flow of the process based on dynamic conditions


## Gateway

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

### Add Object
- Click on object
- Context menu will open
- Select the activity shape
- Update the name

### Change Event Name
- Double click on event
- A text box will open
- Update the name in the text-box
- `shift + Enter` to add line breaks

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
