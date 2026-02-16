# EDR PowerShell Analysis Lab

This lab demonstrates how a suspicious PowerShell process appears in Sysmon logs and how it can be analyzed from a security engineer perspective.

## Objective
Understand how to analyze an EDR alert by focusing on:
- Parent process
- Command line arguments
- Process behavior in logs

## Lab Scenario
A PowerShell process is executed from `cmd.exe` using encoded and policy bypass parameters.

Example command:
powershell.exe -ExecutionPolicy Bypass -enc <encoded_command>


## Key Findings

### Event ID 1 – Process Creation
- Image: powershell.exe
- Parent: cmd.exe
- Command Line: includes `-ExecutionPolicy Bypass` and `-enc`

### Event ID 5 – Process Termination
The PowerShell process terminates shortly after execution.

## Screenshots

### Event ID 1
![Event ID 1](screenshots/event_id_1)

### Command Line
![Command Line](screenshots/event_id_1)


## Tools Used
- Windows
- Sysmon
- Event Viewer
