2025-05-29 22:55

Status: Incomplete

Tags: [[Learning]]

## Creating a simple Script

Structure of the code
1. Event
	Item Usage
	- Different functions - Meaning it can have different effects, ie. Right click or Left Click, Main Hand or Off-hand
	Always use Debug
	event-item: The item that you use in the event ie. Stick, Ender pearl etc
	teleport: teleport 
Example:
'on *%event type%*:' - Always add percent to state changes to be made
	*if event-%event-type% '=' %parameter%*:
		function of the condition

on right click:
    if event-item = stick:
        teleport player to target block

After saving the code, Go to the .../scripts folder of the papermc server, paste the file with the extension of ".sk"

Go back to MC and enter the command
/sk reload '%filename%'

Cancelling an event cancels the event but continues the code

Debugging code means broadcasting or adding a message after a condition
Example
broadcast "%string%"

on right click:
    if event-item = ender pearl:
        cancel event
        broadcast ""
        teleport player to target block


### Reference
